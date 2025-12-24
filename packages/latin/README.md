# Vionous Knowledge Package: Latin Language

A training dataset for teaching AI about Latin language and classical studies.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Latin Language |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 5,843 |
| **Train/Val Split** | 90/10 (5,258 / 585) |
| **Source** | Latin Language Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Latin language and classical studies. The knowledge base is actively maintained and updated by the community.

## Top Topics

|english-to-latin-translation|, |etymology|, |latin-to-english-translation|, |vocabulary|, |english-to-latin-translation|translation-check|, |idiom|, |classical-latin|, |english-to-latin-translation|idiom|, |translation-check|, |english-to-latin-translation|motto|

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
latin/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (5,258 pairs)
│   ├── val.jsonl          (585 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_latin_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/latin/notebooks/vionous_latin_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Latin Language Stack Exchange (https://latin.stackexchange.com)

## Citation

```
Latin Language Stack Exchange
Licensed under CC-BY-SA 4.0
```
