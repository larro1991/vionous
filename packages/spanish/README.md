# Vionous Knowledge Package: Spanish Language

A training dataset for teaching AI about Spanish language learning and linguistics.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Spanish Language |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 8,853 |
| **Train/Val Split** | 90/10 (7,967 / 886) |
| **Source** | Spanish Language Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Spanish language learning and linguistics. The knowledge base is actively maintained and updated by the community.

## Top Topics

|traducción|, |gramática|, |uso-de-palabras|, |selección-de-palabras|, |etimología|, |subjuntivo|, |vocabulario|, |traducción|selección-de-palabras|, |pronunciación|, |solicitud-de-término|

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
spanish/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (7,967 pairs)
│   ├── val.jsonl          (886 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_spanish_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/spanish/notebooks/vionous_spanish_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Spanish Language Stack Exchange (https://spanish.stackexchange.com)

## Citation

```
Spanish Language Stack Exchange
Licensed under CC-BY-SA 4.0
```
