# Vionous Knowledge Package: Expatriates

A training dataset for teaching AI about living and working abroad.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Expatriates |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 5,775 |
| **Train/Val Split** | 90/10 (5,197 / 578) |
| **Source** | Expatriates Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - living and working abroad. The knowledge base is actively maintained and updated by the community.

## Top Topics

|united-kingdom|, |usa|, |usa|greencard|, |germany|, |usa|visa|, |united-kingdom|visa|, |france|, |germany|blue-card|, |visa|, |uk-visa|

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
expatriates/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (5,197 pairs)
│   ├── val.jsonl          (578 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_expatriates_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/expatriates/notebooks/vionous_expatriates_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Expatriates Stack Exchange (https://expatriates.stackexchange.com)

## Citation

```
Expatriates Stack Exchange
Licensed under CC-BY-SA 4.0
```
