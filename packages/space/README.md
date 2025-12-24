# Vionous Knowledge Package: Space Exploration

A training dataset for teaching AI about spaceflight, rockets, and space exploration missions.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Space Exploration |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 16,005 |
| **Train/Val Split** | 90/10 (14,404 / 1,601) |
| **Source** | Space Exploration Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - spaceflight, rockets, and space exploration missions. The knowledge base is actively maintained and updated by the community.

## Top Topics

|orbital-mechanics|, |iss|, |apollo-program|, |artificial-satellite|, |the-moon|, |rockets|, |space-shuttle|, |launch|, |mars|, |james-webb-telescope|

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
space/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (14,404 pairs)
│   ├── val.jsonl          (1,601 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_space_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/space/notebooks/vionous_space_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Space Exploration Stack Exchange (https://space.stackexchange.com)

## Citation

```
Space Exploration Stack Exchange
Licensed under CC-BY-SA 4.0
```
