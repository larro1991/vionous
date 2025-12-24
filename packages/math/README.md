# Vionous Knowledge Package: Mathematics

A training dataset for teaching AI about mathematical concepts, proofs, algebra, calculus, and problem-solving.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Mathematics |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 1,238,770 |
| **Train/Val Split** | 90/10 (1,114,893 / 123,877) |
| **Source** | Mathematics Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - mathematical concepts, proofs, algebra, calculus, and problem-solving. The knowledge base is actively maintained and updated by the community.

## Top Topics

|linear-algebra|, |probability|, |real-analysis|, |calculus|, |general-topology|, |algebra-precalculus|, |complex-analysis|, |ordinary-differential-equations|, |combinatorics|, |geometry|

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
math/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (1,114,893 pairs)
│   ├── val.jsonl          (123,877 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_math_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/math/notebooks/vionous_math_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Mathematics Stack Exchange (https://math.stackexchange.com)

## Citation

```
Mathematics Stack Exchange
Licensed under CC-BY-SA 4.0
```
