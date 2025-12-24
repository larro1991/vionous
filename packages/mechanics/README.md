# Vionous Knowledge Package: Motor Vehicles

A training dataset for teaching AI about vehicle maintenance and repair.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Motor Vehicles |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 20,344 |
| **Train/Val Split** | 90/10 (18,309 / 2,035) |
| **Source** | Motor Vehicles Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - vehicle maintenance and repair. The knowledge base is actively maintained and updated by the community.

## Top Topics

|tires|, |battery|, |engine|, |brakes|, |electrical|, |oil|, |tires|sidewall-damage|, |obd-ii|, |wheels|, |audio|

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
mechanics/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (18,309 pairs)
│   ├── val.jsonl          (2,035 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_mechanics_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/mechanics/notebooks/vionous_mechanics_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Motor Vehicles Stack Exchange (https://mechanics.stackexchange.com)

## Citation

```
Motor Vehicles Stack Exchange
Licensed under CC-BY-SA 4.0
```
