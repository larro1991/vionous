# Vionous Knowledge Package: Freelancing

A training dataset for teaching AI about freelance and self-employment.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Freelancing |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 1,917 |
| **Train/Val Split** | 90/10 (1,725 / 192) |
| **Source** | Freelancing Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - freelance and self-employment. The knowledge base is actively maintained and updated by the community.

## Top Topics

|freelance-websites|, |contracts|, |difficult-client|, |taxes|, |attracting-clients|, |payment-terms|, |invoices|, |pay-rate|, |legal|, |project-management|

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
freelancing/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (1,725 pairs)
│   ├── val.jsonl          (192 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_freelancing_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/freelancing/notebooks/vionous_freelancing_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Freelancing Stack Exchange (https://freelancing.stackexchange.com)

## Citation

```
Freelancing Stack Exchange
Licensed under CC-BY-SA 4.0
```
