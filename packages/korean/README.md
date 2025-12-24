# Vionous Knowledge Package: Korean Language

A training dataset for teaching AI about Korean language learning and linguistics.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Korean Language |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 1,843 |
| **Train/Val Split** | 90/10 (1,658 / 185) |
| **Source** | Korean Language Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Korean language learning and linguistics. The knowledge base is actively maintained and updated by the community.

## Top Topics

|grammar|, |vocabulary|, |pronunciation|, |translation|, |word-usage|, |grammar|meaning|, |grammar|meaning|phrase-meaning|, |meaning|, |hangul|, |word-choice|

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
korean/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (1,658 pairs)
│   ├── val.jsonl          (185 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_korean_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/korean/notebooks/vionous_korean_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Korean Language Stack Exchange (https://korean.stackexchange.com)

## Citation

```
Korean Language Stack Exchange
Licensed under CC-BY-SA 4.0
```
