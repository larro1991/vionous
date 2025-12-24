# Vionous Knowledge Package: Lifehacks

A training dataset for teaching AI about practical life tips and solutions.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Lifehacks |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 2,963 |
| **Train/Val Split** | 90/10 (2,666 / 297) |
| **Source** | Lifehacks Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - practical life tips and solutions. The knowledge base is actively maintained and updated by the community.

## Top Topics

|cleaning|, |clothing|, |personal-care|, |food|, |technology|, |home|, |cleaning|clothing|, |kitchen|, |shoes|, |cleaning|kitchen|

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
lifehacks/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (2,666 pairs)
│   ├── val.jsonl          (297 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_lifehacks_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/lifehacks/notebooks/vionous_lifehacks_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Lifehacks Stack Exchange (https://lifehacks.stackexchange.com)

## Citation

```
Lifehacks Stack Exchange
Licensed under CC-BY-SA 4.0
```
