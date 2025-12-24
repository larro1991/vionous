# Vionous Knowledge Package: History

A training dataset for teaching AI about world history, historical events, and historiography.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | History |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 12,970 |
| **Train/Val Split** | 90/10 (11,673 / 1,297) |
| **Source** | History Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - world history, historical events, and historiography. The knowledge base is actively maintained and updated by the community.

## Top Topics

|world-war-two|, |united-states|, |military|, |ancient-rome|, |ancient-history|, |world-war-one|, |american-civil-war|, |middle-ages|, |world-war-two|nazi-germany|, |historiography|

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
history/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (11,673 pairs)
│   ├── val.jsonl          (1,297 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_history_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/history/notebooks/vionous_history_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from History Stack Exchange (https://history.stackexchange.com)

## Citation

```
History Stack Exchange
Licensed under CC-BY-SA 4.0
```
