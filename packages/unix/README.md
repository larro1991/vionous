# Vionous Knowledge Package: Unix & Linux

A training dataset for teaching AI about Unix and Linux system administration.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Unix & Linux |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 172,180 |
| **Train/Val Split** | 90/10 (154,962 / 17,218) |
| **Source** | Unix & Linux Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Unix and Linux system administration. The knowledge base is actively maintained and updated by the community.

## Top Topics

|bash|, |bash|shell-script|, |shell-script|, |text-processing|, |awk|, |linux|, |sed|, |text-processing|awk|, |ssh|, |grep|

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
unix/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (154,962 pairs)
│   ├── val.jsonl          (17,218 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_unix_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/unix/notebooks/vionous_unix_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Unix & Linux Stack Exchange (https://unix.stackexchange.com)

## Citation

```
Unix & Linux Stack Exchange
Licensed under CC-BY-SA 4.0
```
