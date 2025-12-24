# Vionous Knowledge Package: Biology

A training dataset for teaching AI about genetics, evolution, cell biology, ecology, and biochemistry.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Biology |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 21,912 |
| **Train/Val Split** | 90/10 (19,720 / 2,192) |
| **Source** | Biology Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - genetics, evolution, cell biology, ecology, and biochemistry. The knowledge base is actively maintained and updated by the community.

## Top Topics

|species-identification|entomology|, |evolution|, |genetics|, |human-biology|, |species-identification|, |biochemistry|, |zoology|, |cell-biology|, |species-identification|botany|, |botany|

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
biology/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (19,720 pairs)
│   ├── val.jsonl          (2,192 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_biology_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/biology/notebooks/vionous_biology_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Biology Stack Exchange (https://biology.stackexchange.com)

## Citation

```
Biology Stack Exchange
Licensed under CC-BY-SA 4.0
```
