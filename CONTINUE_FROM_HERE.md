# Vionous Project - Continue From Here

**Last Updated:** December 31, 2024
**Status:** On Hold
**GitHub:** https://github.com/larro1991/vionous

---

## Project Summary

Vionous is an open-source library of AI knowledge packages - modular training datasets for LoRA fine-tuning. The goal is to create domain-specific adapters that can give AI models expertise in various fields.

### What's Complete

| Phase | Status | Details |
|-------|--------|---------|
| Data Collection | **COMPLETE** | 116 packages, 5.77M Q&A pairs |
| Package Structure | **COMPLETE** | All packages have README, SOURCES, LICENSE, training data |
| Notebooks | **COMPLETE** | 117 Colab notebooks for one-click training |
| GitHub Repo | **COMPLETE** | All pushed, Git LFS configured for large files |
| Training Infrastructure | **READY** | Scripts created but no training started |

### What's NOT Started

| Phase | Status | Details |
|-------|--------|---------|
| LoRA Training | **NOT STARTED** | 0 of 24 priority adapters trained |
| Adapter Testing | **NOT STARTED** | No adapters to test yet |
| Hugging Face Upload | **NOT STARTED** | Trained adapters would go here |

---

## Repository Statistics

- **Total Packages:** 116
- **Total Q&A Pairs:** 5,766,117
- **Largest Package:** math (1,238,770 pairs)
- **Repository Size:** ~8 GB (via Git LFS)

### Packages by Category

| Category | Count | Notable |
|----------|-------|---------|
| Science & Math | 14 | math, physics, chemistry, biology, stats |
| Programming | 32 | unix, superuser, tex, salesforce, blender |
| Languages | 14 | english, japanese, german, spanish, french |
| Humanities | 12 | history, philosophy, law, economics |
| Religion | 6 | christianity, islam, judaism, buddhism |
| Arts & Creative | 13 | comics, scifi, gaming, music, rpg |
| Games & Recreation | 10 | chess, puzzling, boardgames, fitness |
| Home & Lifestyle | 12 | cooking, diy, gardening, travel |
| Professional | 11 | workplace, engineering, aviation, 3dprinting |

### Failed Packages (Archive Issues)

These packages failed during data collection due to corrupted archives:
- `quantumcomputing`
- `electronics`
- `security`
- `startups`

To retry, re-run the corresponding section script or manually download/process.

---

## Key Files & Locations

### Main Repository
```
C:\Users\larro\vionous\
├── README.md                    # Main readme with all package listings
├── CONTINUE_FROM_HERE.md        # This file
├── packages/                    # 116 knowledge packages
│   └── [package]/
│       ├── training-data/
│       │   ├── train.jsonl      # Training pairs (90%)
│       │   ├── val.jsonl        # Validation pairs (10%)
│       │   └── stats.json       # Package statistics
│       ├── notebooks/           # Package-specific notebook
│       ├── README.md
│       ├── SOURCES.md
│       └── LICENSE
└── notebooks/                   # All trainer notebooks (117)
```

### Processing Scripts
```
C:\Users\larro\
├── parse_stackexchange.py       # Parses SE Posts.xml to Q&A pairs
├── create_package.py            # Creates package folder structure
├── create_notebook.py           # Generates Colab training notebooks
├── batch_se_processor.py        # Main batch processor for SE sites
├── process_tier1_science.py     # Math, Physics, Chemistry, Biology
├── process_tier1_humanities.py  # English, History
├── process_section1_science.py  # Astronomy, Earth Science, Stats, etc.
├── process_section2_programming.py  # 32 programming sites
├── process_section3_languages.py    # 13 language sites
├── process_section4_humanities.py   # Philosophy, Law, Religion, etc.
├── process_section5_arts.py         # Music, Photo, Movies, etc.
├── process_section6_games.py        # Chess, Sports, Fitness, etc.
├── process_section7_home.py         # DIY, Gardening, Travel, etc.
├── process_section8_professional.py # Workplace, Engineering, etc.
└── regenerate_all_notebooks.py  # Regenerates all notebooks (fixed version)
```

### Training Infrastructure (Ready but unused)
```
C:\Users\larro\vionous-adapters\
├── TRAINING_GUIDE.md            # Detailed training instructions
├── training_log.csv             # Empty CSV for logging results
├── adapter_watcher.py           # Auto-extracts downloaded adapters
├── next_training.py             # Opens next Colab in queue
├── START_WATCHER.bat            # Double-click to start watcher
├── NEXT_TRAINING.bat            # Double-click to open next training
├── SHOW_STATUS.bat              # Double-click to see queue status
└── [24 empty folders]           # Ready for trained adapters
```

### Raw Data
```
C:\Users\larro\vionous_data\
└── [package]/
    ├── Posts.xml                # Raw Stack Exchange data
    └── training-data/           # Processed JSONL files
```

---

## To Continue: Training Adapters

### Training Queue (24 Priority Packages)

**Batch 1 - Quick Wins (~1 hour each):**
1. cooking (25,668 pairs)
2. coffee (1,807 pairs)
3. beer (1,405 pairs)
4. homebrew (8,091 pairs)
5. chess (8,544 pairs)
6. poker (1,933 pairs)
7. latin (4,076 pairs)
8. mythology (2,627 pairs)

**Batch 2 - Medium (~2 hours each):**
1. scifi (65,940 pairs)
2. gaming (90,614 pairs)
3. philosophy (14,296 pairs)
4. history (12,970 pairs)
5. english (113,224 pairs)
6. worldbuilding (25,437 pairs)
7. rpg (67,649 pairs)
8. biology (21,912 pairs)
9. chemistry (34,326 pairs)

**Batch 3 - Large (~3-4 hours each):**
1. physics (175,265 pairs)
2. unix (172,180 pairs)
3. askubuntu (238,910 pairs)
4. serverfault (241,487 pairs)
5. superuser (322,088 pairs)
6. comics (324,621 pairs)
7. math (1,238,770 pairs) - May need reduced epochs

### How to Start Training

1. **Start the watcher** (monitors Downloads for adapter zips):
   ```
   Double-click: C:\Users\larro\vionous-adapters\START_WATCHER.bat
   ```

2. **Open next training**:
   ```
   Double-click: C:\Users\larro\vionous-adapters\NEXT_TRAINING.bat
   ```

3. **In Colab:**
   - Runtime → Change runtime type → T4 GPU
   - Runtime → Run all
   - Wait 1-4 hours
   - Download adapter zip when complete

4. **Watcher auto-extracts** to correct folder and logs result

5. **Repeat** with NEXT_TRAINING.bat

### Training Platform Options

| Platform | Free GPU | Limits |
|----------|----------|--------|
| Google Colab | T4 | ~12 hrs/day, may disconnect |
| Kaggle | P100/T4 | 30 hrs/week |
| Lightning.ai | T4 | 22 hrs/month |

---

## Technical Details

### Model & Training Config

- **Base Model:** Qwen/Qwen2.5-7B-Instruct
- **Quantization:** 4-bit NF4 (BitsAndBytes)
- **LoRA Config:**
  - r=16
  - alpha=32
  - dropout=0.05
  - target_modules: q_proj, k_proj, v_proj, o_proj
- **Training:**
  - 1 epoch
  - batch_size=4, gradient_accumulation=4
  - learning_rate=2e-4
  - max_seq_length=512

### Data Format

Training data is in JSONL format:
```json
{"question": "How do I make a roux?", "answer": "A roux is made by..."}
```

Chat format for Qwen:
```
<|im_start|>user
{question}<|im_end|>
<|im_start|>assistant
{answer}<|im_end|>
```

---

## Future Work Ideas

1. **Train all 24 priority adapters** - Start with Batch 1

2. **Upload to Hugging Face** - Make adapters downloadable
   ```
   huggingface-cli upload larro1991/vionous-cooking ./cooking/
   ```

3. **Retry failed packages** - quantumcomputing, electronics, security, startups

4. **Add more sources:**
   - Open Library books
   - Wikipedia articles
   - arXiv papers
   - Project Gutenberg

5. **Multi-adapter merging** - Combine adapters for multi-domain expertise

6. **Evaluation framework** - Automated testing of adapter quality

---

## GitHub Credentials

**ACTION REQUIRED:** The PAT expired. This document is committed locally but not pushed.

When resuming, first push this commit:
```bash
cd C:\Users\larro\vionous
git push origin main
```

If authentication fails, generate a new PAT:
1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Generate new token with `repo` scope
3. Use token as password when prompted, or update credential manager

---

## Questions to Address When Resuming

1. Should we prioritize training small adapters first to validate the process?
2. Do we want to upload trained adapters to Hugging Face?
3. Should we retry the failed packages?
4. Any new source datasets to add?

---

*Last session: Built complete data pipeline, processed 116 Stack Exchange sites into 5.77M Q&A pairs, created training infrastructure. Ready for LoRA training phase.*
