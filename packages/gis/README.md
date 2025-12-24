# Vionous Knowledge Package: GIS

A training dataset for teaching AI about geographic information systems.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | GIS |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 117,634 |
| **Train/Val Split** | 90/10 (105,870 / 11,764) |
| **Source** | GIS Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - geographic information systems. The knowledge base is actively maintained and updated by the community.

## Top Topics

|qgis|, |google-earth-engine|, |postgis|, |openlayers|, |postgis|postgresql|, |arcgis-maps-sdk-javascript|, |pyqgis|, |arcpy|, |openlayers-2|, |google-earth-engine|google-earth-engine-javascript-api|

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
gis/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (105,870 pairs)
│   ├── val.jsonl          (11,764 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_gis_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/gis/notebooks/vionous_gis_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from GIS Stack Exchange (https://gis.stackexchange.com)

## Citation

```
GIS Stack Exchange
Licensed under CC-BY-SA 4.0
```
