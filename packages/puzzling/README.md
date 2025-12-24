# Vionous Knowledge Package: Puzzling

A training dataset for teaching AI about puzzles and brain teasers.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Puzzling |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 26,274 |
| **Train/Val Split** | 90/10 (23,646 / 2,628) |
| **Source** | Puzzling Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - puzzles and brain teasers. The knowledge base is actively maintained and updated by the community.

## Top Topics

|riddle|, |riddle|word|, |cipher|, |mathematics|, |logical-deduction|, |riddle|rhyme|, |enigmatic-puzzle|, |riddle|wordplay|, |logical-deduction|grid-deduction|, |number-sequence|

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
puzzling/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (23,646 pairs)
│   ├── val.jsonl          (2,628 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_puzzling_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/puzzling/notebooks/vionous_puzzling_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Puzzling Stack Exchange (https://puzzling.stackexchange.com)

## Citation

```
Puzzling Stack Exchange
Licensed under CC-BY-SA 4.0
```
