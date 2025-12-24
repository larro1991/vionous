# Vionous Knowledge Package: Software QA

A training dataset for teaching AI about software testing and quality assurance.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Software QA |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 9,982 |
| **Train/Val Split** | 90/10 (8,983 / 999) |
| **Source** | Software QA Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - software testing and quality assurance. The knowledge base is actively maintained and updated by the community.

## Top Topics

|automated-testing|, |jmeter|, |selenium-webdriver|, |selenium-webdriver|java|, |manual-testing|, |selenium-webdriver|python|, |selenium|, |automated-testing|selenium-webdriver|, |automated-testing|selenium-webdriver|java|, |selenium|webdriver|

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
sqa/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (8,983 pairs)
│   ├── val.jsonl          (999 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_sqa_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/sqa/notebooks/vionous_sqa_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Software QA Stack Exchange (https://sqa.stackexchange.com)

## Citation

```
Software QA Stack Exchange
Licensed under CC-BY-SA 4.0
```
