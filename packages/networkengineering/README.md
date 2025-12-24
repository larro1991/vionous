# Vionous Knowledge Package: Network Engineering

A training dataset for teaching AI about network design and configuration.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Network Engineering |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 15,204 |
| **Train/Val Split** | 90/10 (13,683 / 1,521) |
| **Source** | Network Engineering Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - network design and configuration. The knowledge base is actively maintained and updated by the community.

## Top Topics

|cisco|, |tcp|, |routing|, |wireless|, |vlan|, |ethernet|, |bgp|, |switch|, |network|, |cisco-asa|

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
networkengineering/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (13,683 pairs)
│   ├── val.jsonl          (1,521 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_networkengineering_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/networkengineering/notebooks/vionous_networkengineering_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Network Engineering Stack Exchange (https://networkengineering.stackexchange.com)

## Citation

```
Network Engineering Stack Exchange
Licensed under CC-BY-SA 4.0
```
