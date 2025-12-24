# Vionous Knowledge Package: Ethereum

A training dataset for teaching AI about Ethereum and smart contracts.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Ethereum |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 34,264 |
| **Train/Val Split** | 90/10 (30,837 / 3,427) |
| **Source** | Ethereum Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - Ethereum and smart contracts. The knowledge base is actively maintained and updated by the community.

## Top Topics

|solidity|, |go-ethereum|, |solidity|remix|, |web3js|, |solidity|contract-development|, |contract-development|, |solidity|web3js|, |erc-20|, |transactions|, |blockchain|

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
ethereum/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (30,837 pairs)
│   ├── val.jsonl          (3,427 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_ethereum_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/ethereum/notebooks/vionous_ethereum_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Ethereum Stack Exchange (https://ethereum.stackexchange.com)

## Citation

```
Ethereum Stack Exchange
Licensed under CC-BY-SA 4.0
```
