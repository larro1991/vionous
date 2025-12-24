# Vionous Knowledge Package: Academia

A training dataset for teaching AI about academic life and research.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Academia |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 40,447 |
| **Train/Val Split** | 90/10 (36,402 / 4,045) |
| **Source** | Academia Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - academic life and research. The knowledge base is actively maintained and updated by the community.

## Top Topics

|publications|, |citations|, |graduate-admissions|, |phd|, |peer-review|, |recommendation-letter|, |publications|peer-review|, |research-process|, |phd|graduate-admissions|, |teaching|

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
academia/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (36,402 pairs)
│   ├── val.jsonl          (4,045 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_academia_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/academia/notebooks/vionous_academia_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Academia Stack Exchange (https://academia.stackexchange.com)

## Citation

```
Academia Stack Exchange
Licensed under CC-BY-SA 4.0
```
