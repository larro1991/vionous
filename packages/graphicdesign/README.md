# Vionous Knowledge Package: Graphic Design

A training dataset for teaching AI about graphic design and visual arts.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Graphic Design |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 31,724 |
| **Train/Val Split** | 90/10 (28,551 / 3,173) |
| **Source** | Graphic Design Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - graphic design and visual arts. The knowledge base is actively maintained and updated by the community.

## Top Topics

|adobe-illustrator|, |adobe-photoshop|, |inkscape|, |adobe-indesign|, |gimp|, |font-identification|, |adobe-photoshop|adobe-illustrator|, |fonts|font-identification|, |sketch-app|, |fonts|

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
graphicdesign/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (28,551 pairs)
│   ├── val.jsonl          (3,173 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_graphicdesign_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/graphicdesign/notebooks/vionous_graphicdesign_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Graphic Design Stack Exchange (https://graphicdesign.stackexchange.com)

## Citation

```
Graphic Design Stack Exchange
Licensed under CC-BY-SA 4.0
```
