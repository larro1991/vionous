# Vionous Knowledge Package: Worldbuilding

A training dataset for teaching AI about fictional world creation.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Worldbuilding |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 36,614 |
| **Train/Val Split** | 90/10 (32,952 / 3,662) |
| **Source** | Worldbuilding Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - fictional world creation. The knowledge base is actively maintained and updated by the community.

## Top Topics

|magic|, |science-based|, |internal-consistency|, |science-based|biology|, |creature-design|, |time-travel|, |society|, |biology|, |science-based|internal-consistency|, |weapons|

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
worldbuilding/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (32,952 pairs)
│   ├── val.jsonl          (3,662 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_worldbuilding_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/worldbuilding/notebooks/vionous_worldbuilding_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Worldbuilding Stack Exchange (https://worldbuilding.stackexchange.com)

## Citation

```
Worldbuilding Stack Exchange
Licensed under CC-BY-SA 4.0
```
