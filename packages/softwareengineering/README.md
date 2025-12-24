# Vionous Knowledge Package: Software Engineering

A training dataset for teaching AI about software design, architecture, and development practices.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Software Engineering |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 59,445 |
| **Train/Val Split** | 90/10 (53,500 / 5,945) |
| **Source** | Software Engineering Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - software design, architecture, and development practices. The knowledge base is actively maintained and updated by the community.

## Top Topics

|algorithms|, |java|, |design|, |c#|, |design-patterns|, |domain-driven-design|, |licensing|, |c++|, |unit-testing|, |programming-languages|

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
softwareengineering/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (53,500 pairs)
│   ├── val.jsonl          (5,945 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_softwareengineering_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/softwareengineering/notebooks/vionous_softwareengineering_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Software Engineering Stack Exchange (https://softwareengineering.stackexchange.com)

## Citation

```
Software Engineering Stack Exchange
Licensed under CC-BY-SA 4.0
```
