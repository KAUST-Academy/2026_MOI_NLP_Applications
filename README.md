# KAUST Academy 2026 — NLP Applications (MOI)

Slides and labs for the **2026 KAUST Academy MOI NLP Applications Program**:
two sessions of four days each.

**Course website:** <https://kaust-academy.github.io/2026_MOI_NLP_Applications/>

The site is generated from [`course.toml`](course.toml) by `build.py`, from the
KAUST Academy
[Course_Website_Template](https://github.com/KAUST-Academy/Course_Website_Template).

---

## Schedule

| Session | Day | Topic | Slides | Labs |
|---|---|---|---|---|
| 1 | 1 | NLP Foundations: text, tokens and embeddings | 2 | Text Pre-Processing · Feature Engineering and N-grams · NLP Tasks and Tokenizers · Semantic Search |
| 1 | 2 | Sequence Models and Transformers: RNNs, attention and model families | 2 | RNN, LSTM and GRU on Stack Overflow · Attention-Based Classifier · Encoder, Decoder or Both for QA · Transformer Fine-Tuning |
| 1 | 3 | Large Language Models and Prompting | 2 | How Language Models Behave · Prompting, Measured on Arabic Tweets · Prompt Engineering, Measured |
| 1 | 4 | Running and Fine-Tuning LLMs: quantization, serving, LoRA and preference tuning | 2 | coming soon |
| 2 | 5 | coming soon | coming soon | coming soon |
| 2 | 6 | coming soon | coming soon | coming soon |
| 2 | 7 | coming soon | coming soon | coming soon |
| 2 | 8 | coming soon | coming soon | coming soon |

The labs are written for **Google Colab**; Day 1 Lab 2 and the Day 2 and Day 3
labs are set up for a free T4 GPU. They need internet: they download models, datasets
and NLTK data at runtime.

---

## Repository layout

```
.
├── course.toml          # ALL site content: days, decks, labs. Edit this.
├── build.py             # the generator, standard library only
├── requirements.txt     # what the labs import
├── OFFLINE.md           # classroom delivery without internet
├── theme/               # KAUST Academy theme
├── Slides/Day_N/        # lecture PDFs
├── Labs/Day_N/          # Jupyter notebooks
└── Extra/               # optional references
```

---

## Updating the site

1. Drop the file in `Slides/Day_N/`, `Labs/Day_N/` or `Extra/`.
2. Add or edit its block in [`course.toml`](course.toml) and set
   `status = "ready"`. Give the day a `title`, `blurb` and `icon` when its
   material lands.
3. Check every link resolves, then commit:

   ```bash
   python3 build.py --check     # needs Python 3.11+
   python3 build.py --serve     # preview on http://localhost:8000
   ```

Never edit the generated HTML in `_site/`; it is rebuilt every time.

Each day sets `session = "Session 1"` or `"Session 2"`; the home page groups
the days under one heading per session.

The template's
[README](https://github.com/KAUST-Academy/Course_Website_Template#readme) covers
the rest: the offline bundle, CI, and turning on GitHub Pages.

---

## License

Licensed under [GPL-3.0](LICENSE).

> **Important:** Recording and uploading lectures online is not permitted.
