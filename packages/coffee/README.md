# Vionous Knowledge Package: Coffee

A training dataset for teaching AI about coffee brewing and culture.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Coffee |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 1,336 |
| **Train/Val Split** | 90/10 (1,202 / 134) |
| **Source** | Coffee Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - coffee brewing and culture. The knowledge base is actively maintained and updated by the community.

## Top Topics

|espresso|, |health|, |moka|, |espresso-machine|, |cold-brew|, |flavor|, |ground-coffee|, |beans|, |health|caffeine|, |grinder|

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
coffee/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (1,202 pairs)
│   ├── val.jsonl          (134 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_coffee_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/coffee/notebooks/vionous_coffee_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Coffee Stack Exchange (https://coffee.stackexchange.com)

## Citation

```
Coffee Stack Exchange
Licensed under CC-BY-SA 4.0
```
