# Vionous Knowledge Package: Bicycles

A training dataset for teaching AI about cycling and bicycle maintenance.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Bicycles |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 19,765 |
| **Train/Val Split** | 90/10 (17,788 / 1,977) |
| **Source** | Bicycles Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - cycling and bicycle maintenance. The knowledge base is actively maintained and updated by the community.

## Top Topics

|tire|, |brakes|, |mountain-bike|, |chain|, |identify-this-bike|, |bottom-bracket|, |wheels|, |road-bike|, |crankset|, |frames|

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
bicycles/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (17,788 pairs)
│   ├── val.jsonl          (1,977 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_bicycles_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/bicycles/notebooks/vionous_bicycles_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Bicycles Stack Exchange (https://bicycles.stackexchange.com)

## Citation

```
Bicycles Stack Exchange
Licensed under CC-BY-SA 4.0
```
