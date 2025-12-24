# Vionous Knowledge Package: Salesforce

A training dataset for teaching AI about Salesforce development and administration.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Salesforce |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 95,350 |
| **Train/Val Split** | 90/10 (85,815 / 9,535) |
| **Source** | Salesforce Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - Salesforce development and administration. The knowledge base is actively maintained and updated by the community.

## Top Topics

|apex|, |apex|visualforce|, |visualforce|, |apex|trigger|, |lightning-web-components|, |lightning-aura-components|, |marketing-cloud|ampscript|, |marketing-cloud|, |soql|, |trigger|

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
salesforce/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (85,815 pairs)
│   ├── val.jsonl          (9,535 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_salesforce_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/salesforce/notebooks/vionous_salesforce_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Salesforce Stack Exchange (https://salesforce.stackexchange.com)

## Citation

```
Salesforce Stack Exchange
Licensed under CC-BY-SA 4.0
```
