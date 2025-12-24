# Vionous Knowledge Package: WordPress

A training dataset for teaching AI about WordPress development and customization.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | WordPress |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 77,437 |
| **Train/Val Split** | 90/10 (69,693 / 7,744) |
| **Source** | WordPress Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - WordPress development and customization. The knowledge base is actively maintained and updated by the community.

## Top Topics

|plugins|, |custom-post-types|, |woocommerce-offtopic|, |php|, |categories|, |wp-query|, |plugin-development|, |menus|, |shortcode|, |block-editor|

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
wordpress/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (69,693 pairs)
│   ├── val.jsonl          (7,744 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_wordpress_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/wordpress/notebooks/vionous_wordpress_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from WordPress Stack Exchange (https://wordpress.stackexchange.com)

## Citation

```
WordPress Stack Exchange
Licensed under CC-BY-SA 4.0
```
