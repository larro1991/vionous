# Vionous Knowledge Package: Islam

A training dataset for teaching AI about Islamic theology and practice.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Islam |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 10,969 |
| **Train/Val Split** | 90/10 (9,872 / 1,097) |
| **Source** | Islam Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Islamic theology and practice. The knowledge base is actively maintained and updated by the community.

## Top Topics

|halal-haram|, |salat|, |quran|, |quran|tafseer|, |nikah|, |hadith|source-identification|, |hadith|, |hadith|hadith-interpretation|, |sharia|, |allah|

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
islam/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (9,872 pairs)
│   ├── val.jsonl          (1,097 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_islam_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/islam/notebooks/vionous_islam_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Islam Stack Exchange (https://islam.stackexchange.com)

## Citation

```
Islam Stack Exchange
Licensed under CC-BY-SA 4.0
```
