# Vionous Knowledge Package: Science Fiction & Fantasy

A training dataset for teaching AI about science fiction and fantasy universes, including Star Wars, Star Trek, Lord of the Rings, Harry Potter, Doctor Who, and more.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Science Fiction & Fantasy |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 65,940 |
| **Train/Val Split** | 90/10 (59,346 / 6,594) |
| **Source** | Science Fiction & Fantasy Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - science fiction and fantasy universes, including Star Wars, Star Trek, Lord of the Rings, Harry Potter, Doctor Who, and more. The knowledge base is actively maintained and updated by the community.

## Top Topics

|story-identification|, |harry-potter|, |story-identification|short-stories|, |story-identification|books|, |story-identification|novel|, |story-identification|movie|, |star-wars|, |doctor-who|, |game-of-thrones|a-song-of-ice-and-fire|, |game-of-thrones|

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
scifi/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (59,346 pairs)
│   ├── val.jsonl          (6,594 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_scifi_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/scifi/notebooks/vionous_scifi_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Science Fiction & Fantasy Stack Exchange (https://scifi.stackexchange.com)

## Citation

```
Science Fiction & Fantasy Stack Exchange
Licensed under CC-BY-SA 4.0
```
