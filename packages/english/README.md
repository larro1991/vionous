# Vionous Knowledge Package: English Language

A training dataset for teaching AI about English language usage, grammar, etymology, and linguistics.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | English Language |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 113,224 |
| **Train/Val Split** | 90/10 (101,901 / 11,323) |
| **Source** | English Language Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - English language usage, grammar, etymology, and linguistics. The knowledge base is actively maintained and updated by the community.

## Top Topics

|single-word-requests|, |meaning|, |grammar|, |word-choice|, |word-usage|, |single-word-requests|phrase-requests|, |etymology|, |meaning-in-context|, |expressions|, |grammaticality|

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
english/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (101,901 pairs)
│   ├── val.jsonl          (11,323 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_english_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/english/notebooks/vionous_english_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from English Language Stack Exchange (https://english.stackexchange.com)

## Citation

```
English Language Stack Exchange
Licensed under CC-BY-SA 4.0
```
