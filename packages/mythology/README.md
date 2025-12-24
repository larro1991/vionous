# Vionous Knowledge Package: Mythology

A training dataset for teaching AI about mythology and folklore.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Mythology |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 1,781 |
| **Train/Val Split** | 90/10 (1,602 / 179) |
| **Source** | Mythology Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - mythology and folklore. The knowledge base is actively maintained and updated by the community.

## Top Topics

|greek|, |norse|, |myth-identification|, |egyptian|, |folklore|, |comparative|, |mythical-creatures|, |greek|zeus|, |greek|myth-identification|, |greek|mythical-creatures|

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
mythology/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (1,602 pairs)
│   ├── val.jsonl          (179 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_mythology_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/mythology/notebooks/vionous_mythology_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Mythology Stack Exchange (https://mythology.stackexchange.com)

## Citation

```
Mythology Stack Exchange
Licensed under CC-BY-SA 4.0
```
