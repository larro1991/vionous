# Vionous Knowledge Package: Poker

A training dataset for teaching AI about poker strategy and theory.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Poker |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 1,933 |
| **Train/Val Split** | 90/10 (1,739 / 194) |
| **Source** | Poker Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - poker strategy and theory. The knowledge base is actively maintained and updated by the community.

## Top Topics

|texas-hold-em|, |rules|, |poker-strategy|, |poker-theory|, |odds|, |texas-hold-em|rules|, |probability|, |online|, |tournament|, |betting-strategy|

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
poker/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (1,739 pairs)
│   ├── val.jsonl          (194 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_poker_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/poker/notebooks/vionous_poker_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Poker Stack Exchange (https://poker.stackexchange.com)

## Citation

```
Poker Stack Exchange
Licensed under CC-BY-SA 4.0
```
