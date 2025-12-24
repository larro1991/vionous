# Vionous Training Notebooks

Google Colab notebooks for training LoRA adapters on Vionous knowledge packages.

## Available Notebooks

| Notebook | Package | Q&A Pairs | Est. Time | Colab |
|----------|---------|-----------|-----------|-------|
| [vionous_comics_trainer.ipynb](./vionous_comics_trainer.ipynb) | Comics | 324,621 | ~2-4 hours | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/notebooks/vionous_comics_trainer.ipynb) |
| [vionous_cooking_trainer.ipynb](./vionous_cooking_trainer.ipynb) | Cooking | 25,668 | ~1-2 hours | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/notebooks/vionous_cooking_trainer.ipynb) |
| [vionous_scifi_trainer.ipynb](./vionous_scifi_trainer.ipynb) | SciFi | 65,940 | ~2-3 hours | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/notebooks/vionous_scifi_trainer.ipynb) |
| [vionous_gaming_trainer.ipynb](./vionous_gaming_trainer.ipynb) | Gaming | 90,614 | ~2-3 hours | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/notebooks/vionous_gaming_trainer.ipynb) |

## Requirements

- Google Colab account (free tier works)
- T4 GPU runtime (free)
- ~1-4 hours depending on dataset size

## How to Use

1. Click the "Open in Colab" button for any notebook
2. Go to **Runtime → Change runtime type → T4 GPU**
3. Click **Runtime → Run all**
4. Wait for training to complete
5. Download your LoRA adapter as a zip file

## What You Get

Each notebook produces a LoRA adapter containing:
- `adapter_model.safetensors` - The trained weights
- `adapter_config.json` - Configuration
- Tokenizer files

## Using Your Adapter

```python
from transformers import AutoModelForCausalLM, AutoTokenizer
from peft import PeftModel

# Load base model
base_model = AutoModelForCausalLM.from_pretrained("Qwen/Qwen2.5-7B-Instruct")
tokenizer = AutoTokenizer.from_pretrained("Qwen/Qwen2.5-7B-Instruct")

# Load your trained adapter
model = PeftModel.from_pretrained(base_model, "./your-adapter-folder")

# Generate responses
prompt = "<|im_start|>user\nYour question here<|im_end|>\n<|im_start|>assistant\n"
inputs = tokenizer(prompt, return_tensors="pt")
outputs = model.generate(**inputs, max_new_tokens=200)
print(tokenizer.decode(outputs[0]))
```

## Troubleshooting

### "CUDA out of memory"
- Make sure T4 GPU is selected (not CPU)
- Restart runtime and try again

### Training is slow
- This is expected on free tier GPUs
- Larger datasets take longer

### Colab disconnects
- Keep the browser tab active
- Consider Colab Pro for longer sessions

## License

All notebooks: MIT
Training data: CC-BY-SA 4.0 (see package SOURCES.md for attribution)
