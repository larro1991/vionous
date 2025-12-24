# Vionous Knowledge Package: Gardening

A training dataset for teaching AI about gardening and landscaping.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Gardening |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 15,077 |
| **Train/Val Split** | 90/10 (13,569 / 1,508) |
| **Source** | Gardening Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - gardening and landscaping. The knowledge base is actively maintained and updated by the community.

## Top Topics

|identification|, |trees|, |identification|trees|, |identification|flowers|, |identification|houseplants|, |compost|, |houseplants|, |identification|weeds|, |identification|shrubs|, |tomatoes|

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
gardening/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (13,569 pairs)
│   ├── val.jsonl          (1,508 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_gardening_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/gardening/notebooks/vionous_gardening_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Gardening Stack Exchange (https://gardening.stackexchange.com)

## Citation

```
Gardening Stack Exchange
Licensed under CC-BY-SA 4.0
```
