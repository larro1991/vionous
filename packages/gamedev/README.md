# Vionous Knowledge Package: Game Development

A training dataset for teaching AI about game development and design.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Game Development |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 46,194 |
| **Train/Val Split** | 90/10 (41,574 / 4,620) |
| **Source** | Game Development Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - game development and design. The knowledge base is actively maintained and updated by the community.

## Top Topics

|unity|, |unity|c#|, |c#|unity|, |opengl|, |game-design|, |xna|c#|, |libgdx|, |xna|, |java|libgdx|, |java|

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
gamedev/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (41,574 pairs)
│   ├── val.jsonl          (4,620 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_gamedev_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/gamedev/notebooks/vionous_gamedev_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Game Development Stack Exchange (https://gamedev.stackexchange.com)

## Citation

```
Game Development Stack Exchange
Licensed under CC-BY-SA 4.0
```
