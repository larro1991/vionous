# Vionous Knowledge Package: Chemistry

A training dataset for teaching AI about chemical reactions, organic chemistry, biochemistry, and molecular structures.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Chemistry |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 34,326 |
| **Train/Val Split** | 90/10 (30,893 / 3,433) |
| **Source** | Chemistry Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - chemical reactions, organic chemistry, biochemistry, and molecular structures. The knowledge base is actively maintained and updated by the community.

## Top Topics

|organic-chemistry|, |organic-chemistry|reaction-mechanism|, |inorganic-chemistry|, |thermodynamics|, |organic-chemistry|nomenclature|, |acid-base|, |electrochemistry|, |physical-chemistry|, |everyday-chemistry|, |physical-chemistry|thermodynamics|

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
chemistry/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (30,893 pairs)
│   ├── val.jsonl          (3,433 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_chemistry_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/chemistry/notebooks/vionous_chemistry_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Chemistry Stack Exchange (https://chemistry.stackexchange.com)

## Citation

```
Chemistry Stack Exchange
Licensed under CC-BY-SA 4.0
```
