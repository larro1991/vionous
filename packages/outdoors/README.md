# Vionous Knowledge Package: Outdoors

A training dataset for teaching AI about outdoor activities and hiking.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Outdoors |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 5,864 |
| **Train/Val Split** | 90/10 (5,277 / 587) |
| **Source** | Outdoors Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - outdoor activities and hiking. The knowledge base is actively maintained and updated by the community.

## Top Topics

|hiking|, |fishing|, |backpacks|, |camping|tents|, |sailing|, |gear|, |knots|, |geocaching|, |rock-climbing|, |kayaks|

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
outdoors/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (5,277 pairs)
│   ├── val.jsonl          (587 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_outdoors_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/outdoors/notebooks/vionous_outdoors_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Outdoors Stack Exchange (https://outdoors.stackexchange.com)

## Citation

```
Outdoors Stack Exchange
Licensed under CC-BY-SA 4.0
```
