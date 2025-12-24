# Vionous Knowledge Package: Portuguese Language

A training dataset for teaching AI about Portuguese language learning and linguistics.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Portuguese Language |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 2,344 |
| **Train/Val Split** | 90/10 (2,109 / 235) |
| **Source** | Portuguese Language Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Portuguese language learning and linguistics. The knowledge base is actively maintained and updated by the community.

## Top Topics

|gramática|, |ortografia|, |português-brasileiro|, |etimologia|, |significado|, |tradução-inglês|, |tradução|tradução-inglês|, |pronúncia|, |vocabulário|, |palavra-para-ideia|

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
portuguese/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (2,109 pairs)
│   ├── val.jsonl          (235 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_portuguese_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/portuguese/notebooks/vionous_portuguese_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Portuguese Language Stack Exchange (https://portuguese.stackexchange.com)

## Citation

```
Portuguese Language Stack Exchange
Licensed under CC-BY-SA 4.0
```
