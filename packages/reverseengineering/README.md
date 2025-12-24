# Vionous Knowledge Package: Reverse Engineering

A training dataset for teaching AI about reverse engineering and binary analysis.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Reverse Engineering |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 7,301 |
| **Train/Val Split** | 90/10 (6,570 / 731) |
| **Source** | Reverse Engineering Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - reverse engineering and binary analysis. The knowledge base is actively maintained and updated by the community.

## Top Topics

|ida|, |radare2|, |ida|idapython|, |ollydbg|, |disassembly|, |assembly|, |ghidra|, |firmware|, |ida|disassembly|, |hardware|

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
reverseengineering/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (6,570 pairs)
│   ├── val.jsonl          (731 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_reverseengineering_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/reverseengineering/notebooks/vionous_reverseengineering_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Reverse Engineering Stack Exchange (https://reverseengineering.stackexchange.com)

## Citation

```
Reverse Engineering Stack Exchange
Licensed under CC-BY-SA 4.0
```
