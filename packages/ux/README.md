# Vionous Knowledge Package: UX Design

A training dataset for teaching AI about user experience design.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | UX Design |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 31,277 |
| **Train/Val Split** | 90/10 (28,149 / 3,128) |
| **Source** | UX Design Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - user experience design. The knowledge base is actively maintained and updated by the community.

## Top Topics

|gui-design|, |website-design|, |usability|, |forms|, |terminology|, |navigation|, |icons|, |search|, |usability-testing|, |interaction-design|

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
ux/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (28,149 pairs)
│   ├── val.jsonl          (3,128 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_ux_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/ux/notebooks/vionous_ux_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from UX Design Stack Exchange (https://ux.stackexchange.com)

## Citation

```
UX Design Stack Exchange
Licensed under CC-BY-SA 4.0
```
