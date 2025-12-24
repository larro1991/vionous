# Vionous Knowledge Package: Role-playing Games

A training dataset for teaching AI about tabletop and role-playing games.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Role-playing Games |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 47,151 |
| **Train/Val Split** | 90/10 (42,435 / 4,716) |
| **Source** | Role-playing Games Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - tabletop and role-playing games. The knowledge base is actively maintained and updated by the community.

## Top Topics

|dnd-5e|spells|, |pathfinder-1e|, |dnd-3.5e|, |dnd-4e|, |dnd-5e|magic-items|, |pathfinder-1e|spells|, |dnd-5e|, |dnd-3.5e|spells|, |dnd-5e|monsters|, |pathfinder-1e|magic-items|

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
rpg/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (42,435 pairs)
│   ├── val.jsonl          (4,716 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_rpg_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/rpg/notebooks/vionous_rpg_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Role-playing Games Stack Exchange (https://rpg.stackexchange.com)

## Citation

```
Role-playing Games Stack Exchange
Licensed under CC-BY-SA 4.0
```
