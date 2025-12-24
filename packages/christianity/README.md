# Vionous Knowledge Package: Christianity

A training dataset for teaching AI about Christian theology and practice.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Christianity |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 15,536 |
| **Train/Val Split** | 90/10 (13,982 / 1,554) |
| **Source** | Christianity Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Christian theology and practice. The knowledge base is actively maintained and updated by the community.

## Top Topics

|catholicism|, |bible|, |life-of-jesus|, |lds|, |nature-of-god|, |prayer|, |biblical-basis|, |exegesis|, |terminology|, |soteriology|

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
christianity/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (13,982 pairs)
│   ├── val.jsonl          (1,554 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_christianity_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/christianity/notebooks/vionous_christianity_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Christianity Stack Exchange (https://christianity.stackexchange.com)

## Citation

```
Christianity Stack Exchange
Licensed under CC-BY-SA 4.0
```
