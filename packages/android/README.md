# Vionous Knowledge Package: Android

A training dataset for teaching AI about Android devices and development.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Android |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 32,642 |
| **Train/Val Split** | 90/10 (29,377 / 3,265) |
| **Source** | Android Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - Android devices and development. The knowledge base is actively maintained and updated by the community.

## Top Topics

|google-play-store|, |applications|, |whatsapp-messenger|, |wi-fi|, |rooting|, |sms|, |chrome-for-android|, |contacts|, |adb|, |samsung|

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
android/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (29,377 pairs)
│   ├── val.jsonl          (3,265 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_android_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/android/notebooks/vionous_android_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Android Stack Exchange (https://android.stackexchange.com)

## Citation

```
Android Stack Exchange
Licensed under CC-BY-SA 4.0
```
