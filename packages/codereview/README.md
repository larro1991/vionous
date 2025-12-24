# Vionous Knowledge Package: Code Review

A training dataset for teaching AI about code review and improvement suggestions.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Code Review |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 70,790 |
| **Train/Val Split** | 90/10 (63,711 / 7,079) |
| **Source** | Code Review Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - code review and improvement suggestions. The knowledge base is actively maintained and updated by the community.

## Top Topics

|c#|, |python|, |java|, |javascript|, |javascript|jquery|, |python|python-3.x|, |c++|, |php|, |vba|excel|, |c|

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
codereview/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (63,711 pairs)
│   ├── val.jsonl          (7,079 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_codereview_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/codereview/notebooks/vionous_codereview_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Code Review Stack Exchange (https://codereview.stackexchange.com)

## Citation

```
Code Review Stack Exchange
Licensed under CC-BY-SA 4.0
```
