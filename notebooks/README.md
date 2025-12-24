# Vionous Comics LoRA Trainer

A Google Colab notebook that trains a LoRA adapter to teach Qwen2.5-7B about comic book history.

## Quick Start

### Open in Colab

1. Go to [Google Colab](https://colab.research.google.com/)
2. File → Upload notebook → Select `vionous_comics_trainer.ipynb`
3. **Important:** Runtime → Change runtime type → Select **T4 GPU**
4. Runtime → Run all

Or upload to GitHub and use the "Open in Colab" button.

### What It Does

1. Installs dependencies (transformers, peft, bitsandbytes, trl)
2. Clones the Vionous comics training data from GitHub
3. Loads Qwen2.5-7B-Instruct with 4-bit quantization (fits in T4's 16GB)
4. Configures LoRA (r=16, alpha=32)
5. Trains for 1 epoch on 292K Q&A pairs
6. Tests with comic questions
7. Downloads the adapter as a zip file

## Expected Runtime

| Phase | Time |
|-------|------|
| Install dependencies | ~2 min |
| Clone repo & load data | ~1 min |
| Load model | ~5 min |
| Configure LoRA | ~1 min |
| **Training** | **2-4 hours** |
| Test & download | ~5 min |

**Total: ~2.5-4.5 hours** (mostly training)

## Output

You'll get a zip file containing:
- `adapter_model.safetensors` - The trained LoRA weights
- `adapter_config.json` - LoRA configuration
- Tokenizer files

## Using the Adapter

```python
from transformers import AutoModelForCausalLM, AutoTokenizer
from peft import PeftModel

# Load base model
base_model = AutoModelForCausalLM.from_pretrained(
    "Qwen/Qwen2.5-7B-Instruct",
    device_map="auto"
)
tokenizer = AutoTokenizer.from_pretrained("Qwen/Qwen2.5-7B-Instruct")

# Load your trained adapter
model = PeftModel.from_pretrained(base_model, "./vionous-comics-adapter")

# Ask comic questions!
prompt = "<|im_start|>user\nWhen did Spider-Man first appear?<|im_end|>\n<|im_start|>assistant\n"
inputs = tokenizer(prompt, return_tensors="pt").to(model.device)
outputs = model.generate(**inputs, max_new_tokens=100)
print(tokenizer.decode(outputs[0]))
```

## Training Details

| Parameter | Value |
|-----------|-------|
| Base Model | Qwen/Qwen2.5-7B-Instruct |
| Quantization | 4-bit NF4 |
| LoRA r | 16 |
| LoRA alpha | 32 |
| Target modules | q_proj, k_proj, v_proj, o_proj |
| Batch size | 4 |
| Gradient accumulation | 4 |
| Effective batch size | 16 |
| Learning rate | 2e-4 |
| Epochs | 1 |
| Training examples | 292,158 |

## Troubleshooting

### "CUDA out of memory"
- Make sure you selected T4 GPU (not CPU)
- Runtime → Restart runtime, then Run all again

### Training is slow
- T4 is the free tier GPU; training 292K examples takes time
- Consider reducing dataset size for testing:
  ```python
  train_dataset = train_dataset.select(range(10000))  # Use only 10K examples
  ```

### Colab disconnects
- Keep the browser tab active
- Consider Colab Pro for longer runtimes

## License

Training data: CC-BY-SA 4.0 (from Grand Comics Database)

## Links

- Training Data: https://github.com/larro1991/vionous/tree/main/packages/comics
- Grand Comics Database: https://www.comics.org/
