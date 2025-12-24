# Vionous Knowledge Package: Skeptics

A training dataset for teaching AI about fact-checking and critical thinking.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Skeptics |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 9,104 |
| **Train/Val Split** | 90/10 (8,193 / 911) |
| **Source** | Skeptics Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - fact-checking and critical thinking. The knowledge base is actively maintained and updated by the community.

## Top Topics

|medical-science|, |nutrition|, |united-states|politics|, |quotes|, |history|, |climate-change|, |united-states|, |psychology|, |economics|, |biology|

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
skeptics/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (8,193 pairs)
│   ├── val.jsonl          (911 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_skeptics_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/skeptics/notebooks/vionous_skeptics_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Skeptics Stack Exchange (https://skeptics.stackexchange.com)

## Citation

```
Skeptics Stack Exchange
Licensed under CC-BY-SA 4.0
```
