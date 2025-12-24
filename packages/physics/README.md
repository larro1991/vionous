# Vionous Knowledge Package: Physics

A training dataset for teaching AI about mechanics, electromagnetism, quantum physics, relativity, and thermodynamics.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Physics |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 175,265 |
| **Train/Val Split** | 90/10 (157,738 / 17,527) |
| **Source** | Physics Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - mechanics, electromagnetism, quantum physics, relativity, and thermodynamics. The knowledge base is actively maintained and updated by the community.

## Top Topics

|thermodynamics|, |electromagnetism|, |quantum-mechanics|, |special-relativity|, |newtonian-mechanics|, |electromagnetism|magnetic-fields|, |fluid-dynamics|, |electrostatics|, |optics|, |waves|

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
physics/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (157,738 pairs)
│   ├── val.jsonl          (17,527 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_physics_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/physics/notebooks/vionous_physics_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from Physics Stack Exchange (https://physics.stackexchange.com)

## Citation

```
Physics Stack Exchange
Licensed under CC-BY-SA 4.0
```
