# Vionous Knowledge Package: Project Management

A training dataset for teaching AI about project management practices.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Project Management |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 6,160 |
| **Train/Val Split** | 90/10 (5,544 / 616) |
| **Source** | Project Management Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - project management practices. The knowledge base is actively maintained and updated by the community.

## Top Topics

|ms-project|, |scrum|agile|, |scrum|, |jira|, |agile|, |estimation|, |ms-project|ms-project-2010|, |ms-project|ms-project-2013|, |team-management|, |kanban|

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
pm/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (5,544 pairs)
│   ├── val.jsonl          (616 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_pm_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/pm/notebooks/vionous_pm_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Project Management Stack Exchange (https://pm.stackexchange.com)

## Citation

```
Project Management Stack Exchange
Licensed under CC-BY-SA 4.0
```
