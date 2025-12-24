# Vionous Knowledge Package: Cooking

A training dataset for teaching AI about culinary techniques, recipes, ingredients, and food science.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Cooking |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 25,668 |
| **Train/Val Split** | 90/10 (23,101 / 2,567) |
| **Source** | Cooking Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - culinary techniques, recipes, ingredients, and food science. The knowledge base is actively maintained and updated by the community.

## Top Topics

|food-safety|, |baking|, |bread|, |equipment|, |substitutions|, |baking|bread|, |chicken|, |tea|, |cake|, |coffee|

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
cooking/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (23,101 pairs)
│   ├── val.jsonl          (2,567 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_cooking_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/cooking/notebooks/vionous_cooking_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Cooking Stack Exchange (https://cooking.stackexchange.com)

## Citation

```
Cooking Stack Exchange
Licensed under CC-BY-SA 4.0
```
