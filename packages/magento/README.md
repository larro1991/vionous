# Vionous Knowledge Package: Magento

A training dataset for teaching AI about Magento e-commerce development.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Magento |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 67,089 |
| **Train/Val Split** | 90/10 (60,380 / 6,709) |
| **Source** | Magento Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - Magento e-commerce development. The knowledge base is actively maintained and updated by the community.

## Top Topics

|magento2|, |magento-1.9|, |magento-1.7|, |magento2|magento-2.1|, |magento-1.8|, |magento-2.1|, |magento2|magento2.3|, |magento2.3|, |magento-1.9|php|, |magento2|php|

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
magento/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (60,380 pairs)
│   ├── val.jsonl          (6,709 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_magento_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/magento/notebooks/vionous_magento_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Magento Stack Exchange (https://magento.stackexchange.com)

## Citation

```
Magento Stack Exchange
Licensed under CC-BY-SA 4.0
```
