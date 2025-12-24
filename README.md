# Vionous

### Community-maintained intelligence for everyone.

*Pronounced: VEE-oh-nus — from "vivo" (living) + "nous" (mind)*

---

## What is Vionous?

Vionous is an open-source library of **AI knowledge packages** — modular, trainable datasets that give AI models domain expertise without retraining from scratch.

Instead of every company rebuilding the same knowledge, we build it once and share it freely.

---

## 📦 Available Knowledge Packages

| Package | Q&A Pairs | Temp | Status | Description |
|---------|-----------|------|--------|-------------|
| [Comics](/packages/comics/) | 324,621 | 🌡️ | ✅ Ready | Comic book history, creators, first appearances |
| [Cooking](/packages/cooking/) | 25,668 | 🌡️ | ✅ Ready | Culinary techniques, recipes, food science |
| [SciFi](/packages/scifi/) | 65,940 | 🌡️ | ✅ Ready | Star Wars, Trek, Tolkien, Harry Potter, Doctor Who |
| [Gaming](/packages/gaming/) | 90,614 | 🔥 | ✅ Ready | Video game strategies, walkthroughs, tips |
| Programming | — | 🔥 | 📋 Planned | Stack Overflow knowledge |
| Books & Authors | — | ❄️ | 📋 Planned | Open Library data |

**Total: 506,843 Q&A pairs across 4 packages**

*More packages coming. Want to build one? [See how to contribute](#contributing).*

---

## 🚀 Quick Start

### One-Click Training (Google Colab)

| Package | Train Now |
|---------|-----------|
| Comics | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/notebooks/vionous_comics_trainer.ipynb) |
| Cooking | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/notebooks/vionous_cooking_trainer.ipynb) |
| SciFi | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/notebooks/vionous_scifi_trainer.ipynb) |
| Gaming | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/notebooks/vionous_gaming_trainer.ipynb) |

Train any adapter in ~1-4 hours on a free T4 GPU. No setup required.

### Use a Knowledge Package

```bash
# Clone the repo
git clone https://github.com/larro1991/vionous.git

# Navigate to a package
cd vionous/packages/comics/training-data/

# Training data ready to use
ls -la
# train.jsonl (292K pairs)
# val.jsonl (32K pairs)
```

### Train a LoRA Adapter

```python
# Example using PEFT
from peft import LoraConfig, get_peft_model
from transformers import AutoModelForCausalLM

# Load base model
model = AutoModelForCausalLM.from_pretrained("Qwen/Qwen2.5-7B-Instruct")

# Configure LoRA
lora_config = LoraConfig(
    r=16,
    lora_alpha=32,
    target_modules=["q_proj", "k_proj", "v_proj", "o_proj"],
    lora_dropout=0.05,
)

# Train with your favorite framework (Axolotl, Unsloth, etc.)
```

See [Training Guide](/docs/TRAINING.md) for full instructions.

---

## 💡 How It Works

```
┌─────────────────────────────────────────────────────────┐
│                    Your AI Setup                        │
│                                                         │
│   ┌─────────────┐    ┌──────────────────────────────┐  │
│   │ Base Model  │ +  │ Vionous Adapter(s)           │  │
│   │ (Llama,     │    │ • Comics expertise           │  │
│   │  Mistral,   │    │ • Cooking knowledge          │  │
│   │  Qwen...)   │    │ • Programming skills         │  │
│   └─────────────┘    └──────────────────────────────┘  │
│                                                         │
│   Base model provides general intelligence              │
│   Adapters provide domain expertise                     │
│   Mix and match as needed                               │
└─────────────────────────────────────────────────────────┘
```

**Key insight:** The training data is the real asset. When new model architectures arrive, we regenerate adapters from the same data. Nothing is lost.

---

## 🌡️ Package Temperature System

Knowledge changes at different rates. We track this:

| Temperature | Meaning | Example |
|-------------|---------|---------|
| 🔥 Hot | Rapidly evolving | AI/ML, current events |
| 🌡️ Warm | Stable but updating | Comics, programming |
| ❄️ Cold | Largely complete | Ancient history, classical music |

Resources flow to where they're needed most.

---

## 📊 Package Structure

Every Vionous package follows a standard format:

```
vionous-[domain]/
├── README.md              # What this knows
├── SOURCES.md             # Data attribution
├── LICENSE                # Open license
├── training-data/
│   ├── train.jsonl        # Training pairs
│   └── val.jsonl          # Validation pairs
├── config/
│   └── train_config.yaml  # Training settings
└── tests/
    └── validation_questions.jsonl
```

This means:
- **Portable** — Works with any LoRA training framework
- **Future-proof** — Data survives architecture changes
- **Reproducible** — Anyone can rebuild the adapter

---

## 🤝 Contributing

We need:

| Role | What you'd do |
|------|---------------|
| **Data Curators** | Find and prepare open datasets |
| **Trainers** | Build and test adapters |
| **Domain Experts** | Validate knowledge accuracy |
| **Documenters** | Improve guides and docs |

### Build a New Package

1. Find an open-licensed dataset
2. Transform to Q&A pairs
3. Use our [Package Template](/PACKAGE_TEMPLATE.md)
4. Submit a PR

See [CONTRIBUTING.md](/CONTRIBUTING.md) for details.

---

## 📖 Why Vionous?

Every week, companies spend millions training AI models on the same knowledge that's already been trained elsewhere.

This is wasteful. This is gatekeeping. We can do better.

**Vionous is:**
- Not a company — a commons
- Not a product — infrastructure
- Not controlled — community-governed

Read the full [Manifesto](/MANIFESTO.md).

---

## 📜 License

- Code: MIT
- Knowledge Packages: CC-BY-SA 4.0 (or as specified by source data)

---

## 🔗 Links

- [GitHub Issues](https://github.com/larro1991/vionous/issues) — Report bugs, request features
- [Discussions](https://github.com/larro1991/vionous/discussions) — Introduce yourself, ask questions

---

*"Stop retraining. Start sharing."*
