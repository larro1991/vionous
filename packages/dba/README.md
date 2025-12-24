# Vionous Knowledge Package: Database Administrators

A training dataset for teaching AI about database administration and SQL.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Database Administrators |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 80,973 |
| **Train/Val Split** | 90/10 (72,875 / 8,098) |
| **Source** | Database Administrators Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - database administration and SQL. The knowledge base is actively maintained and updated by the community.

## Top Topics

|sql-server|, |mysql|, |postgresql|, |oracle|, |database-design|, |sql-server|sql-server-2008|, |sql-server|t-sql|, |mongodb|, |sql-server|sql-server-2012|, |mysql|database-design|

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
dba/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (72,875 pairs)
│   ├── val.jsonl          (8,098 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_dba_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/dba/notebooks/vionous_dba_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Database Administrators Stack Exchange (https://dba.stackexchange.com)

## Citation

```
Database Administrators Stack Exchange
Licensed under CC-BY-SA 4.0
```
