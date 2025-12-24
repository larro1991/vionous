# Vionous Knowledge Package: DevOps

A training dataset for teaching AI about DevOps practices and tools.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | DevOps |
| **Temperature** | 🔥 Hot |
| **Q&A Pairs** | 4,547 |
| **Train/Val Split** | 90/10 (4,092 / 455) |
| **Source** | DevOps Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Hot** - DevOps practices and tools. The knowledge base is actively maintained and updated by the community.

## Top Topics

|ansible|, |docker|, |kubernetes|, |jenkins|, |docker|docker-compose|, |terraform|, |jenkins|jenkins-pipeline|, |amazon-web-services|, |gitlab|, |docker|kubernetes|

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
devops/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (4,092 pairs)
│   ├── val.jsonl          (455 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_devops_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/devops/notebooks/vionous_devops_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from DevOps Stack Exchange (https://devops.stackexchange.com)

## Citation

```
DevOps Stack Exchange
Licensed under CC-BY-SA 4.0
```
