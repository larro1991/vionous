# Vionous Knowledge Package: Russian Language

A training dataset for teaching AI about Russian language learning and linguistics.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Russian Language |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 4,576 |
| **Train/Val Split** | 90/10 (4,118 / 458) |
| **Source** | Russian Language Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Russian language learning and linguistics. The knowledge base is actively maintained and updated by the community.

## Top Topics

|грамматика|, |перевод|, |значения|, |словоупотребление|, |выбор-слова|, |произношение|, |пунктуация|, |этимология|, |выражения|, |словоупотребление|значения|

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
russian/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (4,118 pairs)
│   ├── val.jsonl          (458 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_russian_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/russian/notebooks/vionous_russian_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Russian Language Stack Exchange (https://russian.stackexchange.com)

## Citation

```
Russian Language Stack Exchange
Licensed under CC-BY-SA 4.0
```
