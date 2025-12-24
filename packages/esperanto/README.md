# Vionous Knowledge Package: Esperanto Language

A training dataset for teaching AI about Esperanto language learning.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Esperanto Language |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 1,616 |
| **Train/Val Split** | 90/10 (1,454 / 162) |
| **Source** | Esperanto Language Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Esperanto language learning. The knowledge base is actively maintained and updated by the community.

## Top Topics

|single-word-requests|, |translation|, |word-usage|, |word-choice|, |culture|, |pronunciation|, |word-meaning|, |word-difference|, |grammar|, |phrase-requests|

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
esperanto/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (1,454 pairs)
│   ├── val.jsonl          (162 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_esperanto_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/esperanto/notebooks/vionous_esperanto_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Esperanto Language Stack Exchange (https://esperanto.stackexchange.com)

## Citation

```
Esperanto Language Stack Exchange
Licensed under CC-BY-SA 4.0
```
