# Vionous Knowledge Package: Bitcoin

A training dataset for teaching AI about Bitcoin and cryptocurrency development.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Bitcoin |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 25,937 |
| **Train/Val Split** | 90/10 (23,343 / 2,594) |
| **Source** | Bitcoin Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - Bitcoin and cryptocurrency development. The knowledge base is actively maintained and updated by the community.

## Top Topics

|transactions|, |bitcoin-core|, |blockchain|, |wallet|, |bitcoind|, |lightning-network|, |transaction-fees|, |exchanges|, |blockchain.info|, |address|

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
bitcoin/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (23,343 pairs)
│   ├── val.jsonl          (2,594 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_bitcoin_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/bitcoin/notebooks/vionous_bitcoin_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Bitcoin Stack Exchange (https://bitcoin.stackexchange.com)

## Citation

```
Bitcoin Stack Exchange
Licensed under CC-BY-SA 4.0
```
