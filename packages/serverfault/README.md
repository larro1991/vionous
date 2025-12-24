# Vionous Knowledge Package: Server Fault

A training dataset for teaching AI about system administration and IT infrastructure.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Server Fault |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 241,487 |
| **Train/Val Split** | 90/10 (217,338 / 24,149) |
| **Source** | Server Fault Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - system administration and IT infrastructure. The knowledge base is actively maintained and updated by the community.

## Top Topics

|nginx|, |apache-2.2|, |linux|, |mysql|, |domain-name-system|, |postfix|, |untagged|, |active-directory|, |sql-server|, |ssh|

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
serverfault/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (217,338 pairs)
│   ├── val.jsonl          (24,149 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_serverfault_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/serverfault/notebooks/vionous_serverfault_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Server Fault Stack Exchange (https://serverfault.stackexchange.com)

## Citation

```
Server Fault Stack Exchange
Licensed under CC-BY-SA 4.0
```
