# Vionous Knowledge Package: Home Improvement

A training dataset for teaching AI about home improvement and DIY.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Home Improvement |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 70,629 |
| **Train/Val Split** | 90/10 (63,566 / 7,063) |
| **Source** | Home Improvement Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - home improvement and DIY. The knowledge base is actively maintained and updated by the community.

## Top Topics

|electrical|, |plumbing|, |electrical|wiring|, |wiring|, |hvac|, |electrical|electrical-panel|, |electrical-panel|, |electrical|receptacle|, |doors|, |lighting|

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
diy/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (63,566 pairs)
│   ├── val.jsonl          (7,063 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_diy_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/diy/notebooks/vionous_diy_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Home Improvement Stack Exchange (https://diy.stackexchange.com)

## Citation

```
Home Improvement Stack Exchange
Licensed under CC-BY-SA 4.0
```
