# Vionous Knowledge Package: Anime & Manga

A training dataset for teaching AI about anime and manga discussion.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Anime & Manga |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 10,804 |
| **Train/Val Split** | 90/10 (9,723 / 1,081) |
| **Source** | Anime & Manga Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - anime and manga discussion. The knowledge base is actively maintained and updated by the community.

## Top Topics

|naruto|, |one-piece|, |attack-on-titan|, |fairy-tail|, |death-note|, |my-hero-academia|, |bleach|, |anime-production|, |pokemon|, |hunter-x-hunter|

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
anime/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (9,723 pairs)
│   ├── val.jsonl          (1,081 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_anime_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/anime/notebooks/vionous_anime_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Anime & Manga Stack Exchange (https://anime.stackexchange.com)

## Citation

```
Anime & Manga Stack Exchange
Licensed under CC-BY-SA 4.0
```
