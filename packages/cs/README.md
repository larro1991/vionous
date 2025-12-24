# Vionous Knowledge Package: Computer Science

A training dataset for teaching AI about theoretical computer science, algorithms, and complexity.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Computer Science |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 36,545 |
| **Train/Val Split** | 90/10 (32,890 / 3,655) |
| **Source** | Computer Science Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - theoretical computer science, algorithms, and complexity. The knowledge base is actively maintained and updated by the community.

## Top Topics

|algorithms|, |complexity-theory|, |graphs|, |algorithms|graphs|, |computer-architecture|, |asymptotics|, |turing-machines|, |automata|finite-automata|, |formal-languages|regular-languages|, |finite-automata|

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
cs/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (32,890 pairs)
│   ├── val.jsonl          (3,655 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_cs_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/cs/notebooks/vionous_cs_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Computer Science Stack Exchange (https://cs.stackexchange.com)

## Citation

```
Computer Science Stack Exchange
Licensed under CC-BY-SA 4.0
```
