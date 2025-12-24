# Vionous Knowledge Package: Blender

A training dataset for teaching AI about Blender 3D modeling and animation.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Blender |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 68,583 |
| **Train/Val Split** | 90/10 (61,724 / 6,859) |
| **Source** | Blender Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - Blender 3D modeling and animation. The knowledge base is actively maintained and updated by the community.

## Top Topics

|modeling|, |python|, |geometry-nodes|, |animation|, |rendering|, |python|scripting|, |modifiers|, |mesh|, |texturing|, |uv|

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
blender/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (61,724 pairs)
│   ├── val.jsonl          (6,859 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_blender_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/blender/notebooks/vionous_blender_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Blender Stack Exchange (https://blender.stackexchange.com)

## Citation

```
Blender Stack Exchange
Licensed under CC-BY-SA 4.0
```
