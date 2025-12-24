# Vionous Knowledge Package: Literature

A training dataset for teaching AI about literary analysis and interpretation.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Literature |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 5,349 |
| **Train/Val Split** | 90/10 (4,814 / 535) |
| **Source** | Literature Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - literary analysis and interpretation. The knowledge base is actively maintained and updated by the community.

## Top Topics

|identification-request|, |identification-request|short-stories|, |meaning|swimming-in-the-dark|tomasz-jedrowski|, |quote-source|, |meaning|the-childrens-bach|helen-garner|, |j-r-r-tolkien|the-lord-of-the-rings|, |meaning|lord-byron|don-juan|, |meaning|short-stories|g-k-chesterton|father-brown|, |history-of-literature|, |george-orwell|nineteen-eighty-four|

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
literature/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (4,814 pairs)
│   ├── val.jsonl          (535 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_literature_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/literature/notebooks/vionous_literature_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Literature Stack Exchange (https://literature.stackexchange.com)

## Citation

```
Literature Stack Exchange
Licensed under CC-BY-SA 4.0
```
