# Vionous Knowledge Package: 3D Printing

A training dataset for teaching AI about 3D printing technology.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | 3D Printing |
| **Temperature** | 🔥 Hot |
| **Q&A Pairs** | 4,804 |
| **Train/Val Split** | 90/10 (4,323 / 481) |
| **Source** | 3D Printing Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Hot** - 3D printing technology. The knowledge base is actively maintained and updated by the community.

## Top Topics

|print-quality|, |3d-models|, |creality-ender-3|, |ultimaker-cura|, |3d-design|, |filament|, |g-code|, |heated-bed|, |marlin|, |openscad|

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
3dprinting/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (4,323 pairs)
│   ├── val.jsonl          (481 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_3dprinting_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/3dprinting/notebooks/vionous_3dprinting_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from 3D Printing Stack Exchange (https://3dprinting.stackexchange.com)

## Citation

```
3D Printing Stack Exchange
Licensed under CC-BY-SA 4.0
```
