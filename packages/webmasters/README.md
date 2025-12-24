# Vionous Knowledge Package: Webmasters

A training dataset for teaching AI about website operations and SEO.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Webmasters |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 32,300 |
| **Train/Val Split** | 90/10 (29,070 / 3,230) |
| **Source** | Webmasters Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - website operations and SEO. The knowledge base is actively maintained and updated by the community.

## Top Topics

|google-analytics|, |seo|, |google-search-console|, |domains|, |google-adsense|, |seo|google|, |web-hosting|, |mediawiki|, |htaccess|, |seo|google-search|

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
webmasters/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (29,070 pairs)
│   ├── val.jsonl          (3,230 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_webmasters_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/webmasters/notebooks/vionous_webmasters_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Webmasters Stack Exchange (https://webmasters.stackexchange.com)

## Citation

```
Webmasters Stack Exchange
Licensed under CC-BY-SA 4.0
```
