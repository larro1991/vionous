# Vionous Knowledge Package: Operations Research

A training dataset for teaching AI about optimization, linear programming, and decision science.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Operations Research |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 3,251 |
| **Train/Val Split** | 90/10 (2,925 / 326) |
| **Source** | Operations Research Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - optimization, linear programming, and decision science. The knowledge base is actively maintained and updated by the community.

## Top Topics

|optimization|, |mixed-integer-programming|, |linear-programming|, |mixed-integer-programming|modeling|, |mixed-integer-programming|linear-programming|, |modeling|, |optimization|modeling|, |cplex|, |optimization|linear-programming|, |pyomo|

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
or/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (2,925 pairs)
│   ├── val.jsonl          (326 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_or_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/or/notebooks/vionous_or_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Operations Research Stack Exchange (https://or.stackexchange.com)

## Citation

```
Operations Research Stack Exchange
Licensed under CC-BY-SA 4.0
```
