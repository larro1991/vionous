# Vionous Knowledge Package: Chinese Language

A training dataset for teaching AI about Chinese language learning and linguistics.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Chinese Language |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 11,205 |
| **Train/Val Split** | 90/10 (10,084 / 1,121) |
| **Source** | Chinese Language Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Chinese language learning and linguistics. The knowledge base is actively maintained and updated by the community.

## Top Topics

|translation|, |grammar|, |meaning|, |meaning-in-context|, |word-choice|, |vocabulary|, |etymology|, |difference|, |characters|, |pronunciation|

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
chinese/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (10,084 pairs)
│   ├── val.jsonl          (1,121 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_chinese_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/chinese/notebooks/vionous_chinese_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Chinese Language Stack Exchange (https://chinese.stackexchange.com)

## Citation

```
Chinese Language Stack Exchange
Licensed under CC-BY-SA 4.0
```
