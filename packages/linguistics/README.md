# Vionous Knowledge Package: Linguistics

A training dataset for teaching AI about linguistics and language science.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Linguistics |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 8,862 |
| **Train/Val Split** | 90/10 (7,975 / 887) |
| **Source** | Linguistics Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - linguistics and language science. The knowledge base is actively maintained and updated by the community.

## Top Topics

|terminology|, |etymology|, |phonetics|, |phonology|, |syntax|, |computational-linguistics|, |historical-linguistics|, |semantics|, |phonology|phonetics|, |english|

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
linguistics/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (7,975 pairs)
│   ├── val.jsonl          (887 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_linguistics_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/linguistics/notebooks/vionous_linguistics_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Linguistics Stack Exchange (https://linguistics.stackexchange.com)

## Citation

```
Linguistics Stack Exchange
Licensed under CC-BY-SA 4.0
```
