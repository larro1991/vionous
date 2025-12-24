# Vionous Knowledge Package: English Language Learners

A training dataset for teaching AI about English as a second language learning.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | English Language Learners |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 98,227 |
| **Train/Val Split** | 90/10 (88,404 / 9,823) |
| **Source** | English Language Learners Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - English as a second language learning. The knowledge base is actively maintained and updated by the community.

## Top Topics

|grammar|, |meaning|, |meaning-in-context|, |word-usage|, |prepositions|, |word-request|, |word-choice|, |sentence-construction|, |phrase-meaning|, |word-meaning|

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
ell/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (88,404 pairs)
│   ├── val.jsonl          (9,823 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_ell_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/ell/notebooks/vionous_ell_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from English Language Learners Stack Exchange (https://ell.stackexchange.com)

## Citation

```
English Language Learners Stack Exchange
Licensed under CC-BY-SA 4.0
```
