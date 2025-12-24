# Vionous Knowledge Package: Japanese Language

A training dataset for teaching AI about Japanese language learning and linguistics.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Japanese Language |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 27,281 |
| **Train/Val Split** | 90/10 (24,552 / 2,729) |
| **Source** | Japanese Language Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Japanese language learning and linguistics. The knowledge base is actively maintained and updated by the community.

## Top Topics

|grammar|, |meaning|, |translation|, |word-choice|, |words|, |grammar|meaning|, |kanji|, |grammar|translation|, |translation|meaning|, |word-choice|nuances|

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
japanese/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (24,552 pairs)
│   ├── val.jsonl          (2,729 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_japanese_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/japanese/notebooks/vionous_japanese_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Japanese Language Stack Exchange (https://japanese.stackexchange.com)

## Citation

```
Japanese Language Stack Exchange
Licensed under CC-BY-SA 4.0
```
