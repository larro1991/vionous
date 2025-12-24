# Vionous Knowledge Package: Martial Arts

A training dataset for teaching AI about martial arts techniques and training.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Martial Arts |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 2,195 |
| **Train/Val Split** | 90/10 (1,975 / 220) |
| **Source** | Martial Arts Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - martial arts techniques and training. The knowledge base is actively maintained and updated by the community.

## Top Topics

|self-defense|, |training|, |karate|, |tae-kwon-do|, |boxing|, |aikido|, |weapons|, |judo|, |brazilian-jiu-jitsu|, |technique|

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
martialarts/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (1,975 pairs)
│   ├── val.jsonl          (220 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_martialarts_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/martialarts/notebooks/vionous_martialarts_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Martial Arts Stack Exchange (https://martialarts.stackexchange.com)

## Citation

```
Martial Arts Stack Exchange
Licensed under CC-BY-SA 4.0
```
