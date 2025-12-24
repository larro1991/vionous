# Vionous Knowledge Package: Homebrewing

A training dataset for teaching AI about beer and wine brewing.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Homebrewing |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 6,069 |
| **Train/Val Split** | 90/10 (5,462 / 607) |
| **Source** | Homebrewing Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - beer and wine brewing. The knowledge base is actively maintained and updated by the community.

## Top Topics

|fermentation|, |yeast|, |cider|, |beer|, |hops|, |carbonation|, |kegging|, |wine|, |water|, |bottling|

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
homebrew/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (5,462 pairs)
│   ├── val.jsonl          (607 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_homebrew_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/homebrew/notebooks/vionous_homebrew_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Homebrewing Stack Exchange (https://homebrew.stackexchange.com)

## Citation

```
Homebrewing Stack Exchange
Licensed under CC-BY-SA 4.0
```
