# Vionous Knowledge Package: Aviation

A training dataset for teaching AI about aviation and flight.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Aviation |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 23,329 |
| **Train/Val Split** | 90/10 (20,996 / 2,333) |
| **Source** | Aviation Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - aviation and flight. The knowledge base is actively maintained and updated by the community.

## Top Topics

|aerodynamics|, |aircraft-design|, |aircraft-identification|, |faa-regulations|, |air-traffic-control|, |jet-engine|, |aircraft-performance|, |safety|, |aircraft-design|aerodynamics|, |aircraft-maintenance|

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
aviation/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (20,996 pairs)
│   ├── val.jsonl          (2,333 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_aviation_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/aviation/notebooks/vionous_aviation_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Aviation Stack Exchange (https://aviation.stackexchange.com)

## Citation

```
Aviation Stack Exchange
Licensed under CC-BY-SA 4.0
```
