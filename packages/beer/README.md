# Vionous Knowledge Package: Beer

A training dataset for teaching AI about beer styles and appreciation.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Beer |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 1,118 |
| **Train/Val Split** | 90/10 (1,006 / 112) |
| **Source** | Beer Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - beer styles and appreciation. The knowledge base is actively maintained and updated by the community.

## Top Topics

|wine|, |brewing|, |taste|, |health|, |specialty-beers|, |whiskey|, |breweries|, |storage|, |history|, |pairing|

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
beer/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (1,006 pairs)
│   ├── val.jsonl          (112 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_beer_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/beer/notebooks/vionous_beer_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Beer Stack Exchange (https://beer.stackexchange.com)

## Citation

```
Beer Stack Exchange
Licensed under CC-BY-SA 4.0
```
