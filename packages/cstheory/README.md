# Vionous Knowledge Package: Theoretical CS

A training dataset for teaching AI about research-level theoretical computer science.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Theoretical CS |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 9,044 |
| **Train/Val Split** | 90/10 (8,139 / 905) |
| **Source** | Theoretical CS Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - research-level theoretical computer science. The knowledge base is actively maintained and updated by the community.

## Top Topics

|cc.complexity-theory|, |ds.algorithms|, |graph-theory|graph-algorithms|, |cc.complexity-theory|complexity-classes|, |graph-theory|, |soft-question|, |quantum-computing|, |cg.comp-geom|, |ds.data-structures|, |cr.crypto-security|

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
cstheory/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (8,139 pairs)
│   ├── val.jsonl          (905 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_cstheory_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/cstheory/notebooks/vionous_cstheory_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Theoretical CS Stack Exchange (https://cstheory.stackexchange.com)

## Citation

```
Theoretical CS Stack Exchange
Licensed under CC-BY-SA 4.0
```
