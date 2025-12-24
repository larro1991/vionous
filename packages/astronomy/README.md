# Vionous Knowledge Package: Astronomy

A training dataset for teaching AI about astronomy, astrophysics, and space observation.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Astronomy |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 12,405 |
| **Train/Val Split** | 90/10 (11,164 / 1,241) |
| **Source** | Astronomy Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - astronomy, astrophysics, and space observation. The knowledge base is actively maintained and updated by the community.

## Top Topics

|star|, |telescope|, |black-hole|, |the-moon|, |the-sun|, |observational-astronomy|, |universe|, |galaxy|, |orbit|, |solar-eclipse|

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
astronomy/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (11,164 pairs)
│   ├── val.jsonl          (1,241 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_astronomy_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/astronomy/notebooks/vionous_astronomy_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Astronomy Stack Exchange (https://astronomy.stackexchange.com)

## Citation

```
Astronomy Stack Exchange
Licensed under CC-BY-SA 4.0
```
