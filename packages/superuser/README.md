# Vionous Knowledge Package: Super User

A training dataset for teaching AI about computer hardware and software help.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Super User |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 322,088 |
| **Train/Val Split** | 90/10 (289,879 / 32,209) |
| **Source** | Super User Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - computer hardware and software help. The knowledge base is actively maintained and updated by the community.

## Top Topics

|microsoft-excel|, |microsoft-excel|worksheet-function|, |windows-7|, |windows|, |windows-10|, |linux|, |google-chrome|, |microsoft-word|, |ffmpeg|, |vim|

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
superuser/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (289,879 pairs)
│   ├── val.jsonl          (32,209 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_superuser_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/superuser/notebooks/vionous_superuser_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Super User Stack Exchange (https://superuser.stackexchange.com)

## Citation

```
Super User Stack Exchange
Licensed under CC-BY-SA 4.0
```
