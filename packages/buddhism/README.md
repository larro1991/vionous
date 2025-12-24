# Vionous Knowledge Package: Buddhism

A training dataset for teaching AI about Buddhist philosophy and practice.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Buddhism |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 8,192 |
| **Train/Val Split** | 90/10 (7,372 / 820) |
| **Source** | Buddhism Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Buddhist philosophy and practice. The knowledge base is actively maintained and updated by the community.

## Top Topics

|theravada|, |meditation|, |karma|, |personal-practice|, |pali-canon|, |the-buddha|, |philosophy|, |vipassana|, |nirvana|, |reference-request|

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
buddhism/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (7,372 pairs)
│   ├── val.jsonl          (820 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_buddhism_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/buddhism/notebooks/vionous_buddhism_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Buddhism Stack Exchange (https://buddhism.stackexchange.com)

## Citation

```
Buddhism Stack Exchange
Licensed under CC-BY-SA 4.0
```
