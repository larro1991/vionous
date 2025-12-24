# Vionous Knowledge Package: Engineering

A training dataset for teaching AI about engineering practices and design.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Engineering |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 11,416 |
| **Train/Val Split** | 90/10 (10,274 / 1,142) |
| **Source** | Engineering Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - engineering practices and design. The knowledge base is actively maintained and updated by the community.

## Top Topics

|mechanical-engineering|, |electrical-engineering|, |structural-engineering|, |fluid-mechanics|, |materials|, |thermodynamics|, |control-engineering|control-theory|, |mechanical-engineering|gears|, |civil-engineering|, |structural-engineering|structural-analysis|

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
engineering/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (10,274 pairs)
│   ├── val.jsonl          (1,142 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_engineering_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/engineering/notebooks/vionous_engineering_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Engineering Stack Exchange (https://engineering.stackexchange.com)

## Citation

```
Engineering Stack Exchange
Licensed under CC-BY-SA 4.0
```
