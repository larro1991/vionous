# Vionous Knowledge Package: Amateur Radio

A training dataset for teaching AI about amateur radio and communications.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Amateur Radio |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 4,422 |
| **Train/Val Split** | 90/10 (3,979 / 443) |
| **Source** | Amateur Radio Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - amateur radio and communications. The knowledge base is actively maintained and updated by the community.

## Top Topics

|antenna|, |antenna-theory|, |antenna|antenna-theory|, |cw|, |rfi|, |software-defined-radio|gnuradio|, |software-defined-radio|, |united-states|license|, |repeater|, |satellites|

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
ham/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (3,979 pairs)
│   ├── val.jsonl          (443 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_ham_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/ham/notebooks/vionous_ham_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Amateur Radio Stack Exchange (https://ham.stackexchange.com)

## Citation

```
Amateur Radio Stack Exchange
Licensed under CC-BY-SA 4.0
```
