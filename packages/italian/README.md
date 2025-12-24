# Vionous Knowledge Package: Italian Language

A training dataset for teaching AI about Italian language learning and linguistics.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Italian Language |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 3,465 |
| **Train/Val Split** | 90/10 (3,118 / 347) |
| **Source** | Italian Language Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Italian language learning and linguistics. The knowledge base is actively maintained and updated by the community.

## Top Topics

|meaning|, |word-meaning|, |grammar|, |word-meaning|verbs|, |word-usage|, |translation|, |word-meaning|regional|, |meaning|idioms|, |etymology|, |verbs|

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
italian/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (3,118 pairs)
│   ├── val.jsonl          (347 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_italian_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/italian/notebooks/vionous_italian_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Italian Language Stack Exchange (https://italian.stackexchange.com)

## Citation

```
Italian Language Stack Exchange
Licensed under CC-BY-SA 4.0
```
