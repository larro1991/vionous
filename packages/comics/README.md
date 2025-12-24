# Vionous Knowledge Package: Comics

A comprehensive training dataset for teaching AI about comic book history, creators, characters, and publication data.

## Overview

| Property | Value |
|----------|-------|
| **Domain** | Comic Books & Graphic Novels |
| **Temperature** | Warm |
| **Q&A Pairs** | 324,621 |
| **Train/Val Split** | 90/10 (292,158 / 32,463) |
| **Source** | Grand Comics Database (GCD) |
| **License** | CC-BY-SA 4.0 |
| **Compatible** | Llama architecture models |

## Temperature Explanation

**Warm** - Comic book history is an active, evolving domain. New issues are published weekly, creators continue their careers, and characters are constantly reintroduced or reimagined. While this dataset covers established historical facts (first appearances, publication dates, creator credits), the broader comics landscape continues to evolve. Best used for historical knowledge through 2021.

## Dataset Contents

### Q&A Type Distribution

| Type | Count | Percentage |
|------|-------|------------|
| Issue Counts | 70,303 | 21.7% |
| Series Summaries | 70,141 | 21.6% |
| Publication Dates | 69,826 | 21.5% |
| First Appearances | 23,600 | 7.3% |
| Pricing Info | 15,675 | 4.8% |
| Genre Classification | 13,912 | 4.3% |
| Content Descriptions | 8,111 | 2.5% |
| Character Appearances | 734 | 0.2% |
| Reprints | 209 | 0.1% |
| Other | 51,997 | 16.0% |

### Temporal Coverage

Comics data spans from the 1860s to 2021, with strongest coverage in:
- 2000s: 91,854 mentions
- 1990s: 86,427 mentions
- 2010s: 61,464 mentions
- 1980s: 47,713 mentions
- 1970s: 30,668 mentions

### Content Coverage

- **150,000+** comic series
- **14,000+** publishers
- **47,000+** creators
- **13,000+** character features with genre/year data

## Example Q&A Pairs

```json
{"question": "When did Spider-Man first appear in comics?", "answer": "Spider-Man first appeared in comics in 1962. They are a superhero character/feature."}

{"question": "What comics did Jack Kirby work on?", "answer": "Jack Kirby worked on: Fantastic Four, Captain America, Thor, New Gods, The Eternals, Mister Miracle, OMAC, Kamandi..."}

{"question": "How many issues of 'Batman' were published?", "answer": "'Batman' had 713 issues published from 1940 to 2011."}

{"question": "Was the story from Batman #64 ever reprinted?", "answer": "Yes! The story from Batman #64 was reprinted in: Batman #113."}

{"question": "What type of character is Wolverine?", "answer": "Wolverine is a superhero character/feature in comics."}
```

## File Structure

```
vionous-comics/
├── README.md              # This file
├── SOURCES.md             # Data source credits and methodology
├── LICENSE                # CC-BY-SA 4.0 license
├── training-data/
│   ├── train.jsonl        # Training data (292,158 pairs)
│   ├── val.jsonl          # Validation data (32,463 pairs)
│   └── stats.json         # Dataset statistics
├── config/
│   └── train_config.yaml  # Suggested training configuration
└── tests/
    └── validation_questions.jsonl  # Manual test questions
```

## Usage

### With Axolotl

```yaml
base_model: meta-llama/Llama-3.2-3B-Instruct
datasets:
  - path: ./training-data/train.jsonl
    type: sharegpt
val_set_size: 0.1
```

### With Unsloth

```python
from unsloth import FastLanguageModel
from datasets import load_dataset

dataset = load_dataset("json", data_files="training-data/train.jsonl")
```

### Direct Loading

```python
import json

with open("training-data/train.jsonl") as f:
    data = [json.loads(line) for line in f]
```

## Quality Notes

- Data sourced from GCD, a community-maintained database with editorial oversight
- Some entries may contain uncertain attributions (marked with "?" in original data)
- First appearance data derived from notes and feature metadata
- Pricing in original currency (USD, GBP, etc.)

## Citation

If you use this dataset, please credit:

```
Grand Comics Database (https://www.comics.org/)
Licensed under CC-BY-SA 4.0
```

## Version History

- **1.0.0** (2024-12): Initial release from GCD 2021-05-29 dump
