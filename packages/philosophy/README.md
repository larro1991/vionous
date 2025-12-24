# Vionous Knowledge Package: Philosophy

A training dataset for teaching AI about philosophy, ethics, and logic.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Philosophy |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 18,258 |
| **Train/Val Split** | 90/10 (16,432 / 1,826) |
| **Source** | Philosophy Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - philosophy, ethics, and logic. The knowledge base is actively maintained and updated by the community.

## Top Topics

|logic|, |ethics|, |fallacies|, |philosophy-of-science|, |philosophy-of-mathematics|, |metaphysics|, |logic|fallacies|, |epistemology|, |philosophy-of-mind|, |reference-request|

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
philosophy/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (16,432 pairs)
│   ├── val.jsonl          (1,826 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_philosophy_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/philosophy/notebooks/vionous_philosophy_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Philosophy Stack Exchange (https://philosophy.stackexchange.com)

## Citation

```
Philosophy Stack Exchange
Licensed under CC-BY-SA 4.0
```
