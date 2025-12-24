# Vionous Knowledge Package: Law

A training dataset for teaching AI about legal questions and jurisprudence.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Law |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 26,024 |
| **Train/Val Split** | 90/10 (23,421 / 2,603) |
| **Source** | Law Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - legal questions and jurisprudence. The knowledge base is actively maintained and updated by the community.

## Top Topics

|copyright|, |contract-law|, |united-states|, |gdpr|, |criminal-law|, |united-kingdom|, |trademark|, |united-states|criminal-law|, |copyright|intellectual-property|, |legal-terms|

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
law/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (23,421 pairs)
│   ├── val.jsonl          (2,603 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_law_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/law/notebooks/vionous_law_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Law Stack Exchange (https://law.stackexchange.com)

## Citation

```
Law Stack Exchange
Licensed under CC-BY-SA 4.0
```
