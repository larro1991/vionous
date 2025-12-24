# Vionous Knowledge Package: Physical Fitness

A training dataset for teaching AI about exercise and fitness training.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Physical Fitness |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 9,265 |
| **Train/Val Split** | 90/10 (8,338 / 927) |
| **Source** | Physical Fitness Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - exercise and fitness training. The knowledge base is actively maintained and updated by the community.

## Top Topics

|running|, |weightlifting|, |exercise|, |weight-loss|, |workout|, |workout-routines|, |swimming|, |push-ups|, |diet|, |cardio|

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
fitness/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (8,338 pairs)
│   ├── val.jsonl          (927 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_fitness_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/fitness/notebooks/vionous_fitness_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Physical Fitness Stack Exchange (https://fitness.stackexchange.com)

## Citation

```
Physical Fitness Stack Exchange
Licensed under CC-BY-SA 4.0
```
