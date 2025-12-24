# Vionous Knowledge Package: TeX LaTeX

A training dataset for teaching AI about TeX, LaTeX, and document typesetting.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | TeX LaTeX |
| **Temperature** | ❄️ Cold |
| **Q&A Pairs** | 207,423 |
| **Train/Val Split** | 90/10 (186,680 / 20,743) |
| **Source** | TeX LaTeX Stack Exchange |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Cold** - TeX, LaTeX, and document typesetting. The knowledge base is actively maintained and updated by the community.

## Top Topics

|tikz-pgf|, |tables|, |biblatex|, |pgfplots|, |tikz-pgf|pgfplots|, |beamer|, |macros|, |math-mode|, |symbols|, |fonts|

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
tex/
├── README.md
├── SOURCES.md
├── LICENSE
├── training-data/
│   ├── train.jsonl        (186,680 pairs)
│   ├── val.jsonl          (20,743 pairs)
│   └── stats.json
├── config/
│   └── train_config.yaml
├── tests/
│   └── validation_questions.jsonl
└── notebooks/
    └── vionous_tex_trainer.ipynb
```

## Usage

### Quick Start (Google Colab)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larro1991/vionous/blob/main/packages/tex/notebooks/vionous_tex_trainer.ipynb)

### Manual Training

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

## License

CC-BY-SA 4.0 - See LICENSE file

Data sourced from TeX LaTeX Stack Exchange (https://tex.stackexchange.com)

## Citation

```
TeX LaTeX Stack Exchange
Licensed under CC-BY-SA 4.0
```
