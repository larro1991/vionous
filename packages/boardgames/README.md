# Vionous Knowledge Package: Board Games

A training dataset for teaching AI about board and card games.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Board Games |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 13,322 |
| **Train/Val Split** | 90/10 (11,989 / 1,333) |
| **Source** | Board Games Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - board and card games. The knowledge base is actively maintained and updated by the community.

## Top Topics

|magic-the-gathering|, |identify-this-game|, |yu-gi-oh|, |bridge|bidding|, |magic-the-gathering|mtg-commander|, |catan|, |bridge|, |android-netrunner|, |arkham-horror|, |monopoly|

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
boardgames/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (11,989 pairs)
│   ├── val.jsonl          (1,333 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_boardgames_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/boardgames/notebooks/vionous_boardgames_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Board Games Stack Exchange (https://boardgames.stackexchange.com)

## Citation

```
Board Games Stack Exchange
Licensed under CC-BY-SA 4.0
```
