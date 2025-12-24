# Vionous Knowledge Package: Judaism

A training dataset for teaching AI about Jewish law and tradition.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Judaism |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 31,370 |
| **Train/Val Split** | 90/10 (28,233 / 3,137) |
| **Source** | Judaism Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - Jewish law and tradition. The knowledge base is actively maintained and updated by the community.

## Top Topics

|purim-torah-in-jest|, |mi-yodeya-series|number|, |number|mi-yodeya-series|, |halacha|, |kashrut-kosher|, |tefilla|, |hashkafah-philosophy|, |talmud-gemara|, |sources-mekorot|, |tanach|

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
judaism/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (28,233 pairs)
│   ├── val.jsonl          (3,137 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_judaism_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/judaism/notebooks/vionous_judaism_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Judaism Stack Exchange (https://judaism.stackexchange.com)

## Citation

```
Judaism Stack Exchange
Licensed under CC-BY-SA 4.0
```
