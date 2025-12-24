# Vionous Knowledge Package: Earth Science

A training dataset for teaching AI about geology, meteorology, oceanography, and environmental science.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Earth Science |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 5,363 |
| **Train/Val Split** | 90/10 (4,826 / 537) |
| **Source** | Earth Science Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - geology, meteorology, oceanography, and environmental science. The knowledge base is actively maintained and updated by the community.

## Top Topics

|climate-change|, |meteorology|, |geology|, |atmosphere|, |earthquakes|, |geophysics|, |geography|, |oceanography|, |meteorology|weather-forecasting|, |hydrology|models|

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
earthscience/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (4,826 pairs)
│   ├── val.jsonl          (537 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_earthscience_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/earthscience/notebooks/vionous_earthscience_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Earth Science Stack Exchange (https://earthscience.stackexchange.com)

## Citation

```
Earth Science Stack Exchange
Licensed under CC-BY-SA 4.0
```
