# Vionous Knowledge Package: Hinduism

A training dataset for teaching AI about Hindu philosophy and practice.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Hinduism |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 11,346 |
| **Train/Val Split** | 90/10 (10,211 / 1,135) |
| **Source** | Hinduism Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Hindu philosophy and practice. The knowledge base is actively maintained and updated by the community.

## Top Topics

|mahabharata|, |bhagavad-gita|, |vedas|, |gods|, |scripture|, |mantras|, |karma|, |shiva|, |ramayana|, |krishna|

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
hinduism/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (10,211 pairs)
│   ├── val.jsonl          (1,135 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_hinduism_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/hinduism/notebooks/vionous_hinduism_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Hinduism Stack Exchange (https://hinduism.stackexchange.com)

## Citation

```
Hinduism Stack Exchange
Licensed under CC-BY-SA 4.0
```
