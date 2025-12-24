# Vionous Knowledge Package: Sustainability

A training dataset for teaching AI about sustainable living practices.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Sustainability |
| **Temperature** | 🔥 Hot |
| **Q&A Pairs** | 1,965 |
| **Train/Val Split** | 90/10 (1,768 / 197) |
| **Source** | Sustainability Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Hot** - sustainable living practices. The knowledge base is actively maintained and updated by the community.

## Top Topics

|solar-power|, |composting|, |recycling|, |recycling|plastic|, |waste|, |heating|, |batteries|, |energy|, |aquaponics|, |composting|vermicomposting|

## Dataset Contents

Training pairs derived from Stack Exchange Q&A:
- Questions with accepted or high-scoring answers
- Filtered for quality (Score >= 1)
- HTML cleaned, code blocks preserved

## Example Q&A Pairs

```json
{"question": "How do I [common task]?", "answer": "Here's how to do it..."}
```

## File Structure

```
sustainability/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (1,768 pairs)
│   ├── val.jsonl          (197 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_sustainability_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/sustainability/notebooks/vionous_sustainability_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Sustainability Stack Exchange (https://sustainability.stackexchange.com)

## Citation

```
Sustainability Stack Exchange
Licensed under CC-BY-SA 4.0
```
