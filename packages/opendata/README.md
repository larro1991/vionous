# Vionous Knowledge Package: Open Data

A training dataset for teaching AI about open data and data access.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Open Data |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 3,983 |
| **Train/Val Split** | 90/10 (3,584 / 399) |
| **Source** | Open Data Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - open data and data access. The knowledge base is actively maintained and updated by the community.

## Top Topics

|data-request|, |openfda|, |mimic-iii|, |data-request|geospatial|, |geospatial|, |collegescorecard|, |data-request|medical|, |api|openfda|, |wikidata|sparql|, |data-request|sports|

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
opendata/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (3,584 pairs)
│   ├── val.jsonl          (399 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_opendata_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/opendata/notebooks/vionous_opendata_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Open Data Stack Exchange (https://opendata.stackexchange.com)

## Citation

```
Open Data Stack Exchange
Licensed under CC-BY-SA 4.0
```
