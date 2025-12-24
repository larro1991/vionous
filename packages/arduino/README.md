# Vionous Knowledge Package: Arduino

A training dataset for teaching AI about Arduino programming and electronics.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Arduino |
| **Temperature** | 🌡️ Warm |
| **Q&A Pairs** | 20,064 |
| **Train/Val Split** | 90/10 (18,057 / 2,007) |
| **Source** | Arduino Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - Arduino programming and electronics. The knowledge base is actively maintained and updated by the community.

## Top Topics

|arduino-uno|, |arduino-mega|, |esp8266|, |serial|, |programming|, |sensors|, |arduino-ide|, |arduino-nano|, |arduino-uno|sensors|, |arduino-uno|esp8266|

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
arduino/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (18,057 pairs)
│   ├── val.jsonl          (2,007 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_arduino_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/arduino/notebooks/vionous_arduino_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Arduino Stack Exchange (https://arduino.stackexchange.com)

## Citation

```
Arduino Stack Exchange
Licensed under CC-BY-SA 4.0
```
