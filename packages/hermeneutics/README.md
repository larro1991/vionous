# Vionous Knowledge Package: Biblical Hermeneutics

A training dataset for teaching AI about biblical interpretation and exegesis.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Biblical Hermeneutics |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 14,121 |
| **Train/Val Split** | 90/10 (12,708 / 1,413) |
| **Source** | Biblical Hermeneutics Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - biblical interpretation and exegesis. The knowledge base is actively maintained and updated by the community.

## Top Topics

|genesis|, |john|, |matthew|, |revelation|, |isaiah|, |psalms|, |exodus|, |luke|, |acts|, |romans|

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
hermeneutics/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (12,708 pairs)
│   ├── val.jsonl          (1,413 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_hermeneutics_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/hermeneutics/notebooks/vionous_hermeneutics_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Biblical Hermeneutics Stack Exchange (https://hermeneutics.stackexchange.com)

## Citation

```
Biblical Hermeneutics Stack Exchange
Licensed under CC-BY-SA 4.0
```
