# Vionous Knowledge Package: Music

A training dataset for teaching AI about music theory and practice.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Music |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 24,332 |
| **Train/Val Split** | 90/10 (21,898 / 2,434) |
| **Source** | Music Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - music theory and practice. The knowledge base is actively maintained and updated by the community.

## Top Topics

|piano|, |theory|, |lilypond|, |voice|, |guitar|, |notation|, |electric-guitar|, |chords|, |chord-theory|, |piano|fingering|

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
music/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (21,898 pairs)
│   ├── val.jsonl          (2,434 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_music_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/music/notebooks/vionous_music_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Music Stack Exchange (https://music.stackexchange.com)

## Citation

```
Music Stack Exchange
Licensed under CC-BY-SA 4.0
```
