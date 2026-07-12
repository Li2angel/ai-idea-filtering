# AI-Assisted Idea Filtering

A research project comparing LLM-based methods for shortlisting the most 
promising ideas in large online deliberations.

**Author:** Mustapha Babatunde Abimbola  
**Supervisor:** Prof. Mark Klein  
**Institution:** School of Collective Intelligence, Mohammed VI Polytechnic University  
**Year:** 2025–2026

---

## What this project does

Online deliberation platforms collect more ideas than reviewers can read.
This project compares five AI-based filtering methods that automatically 
shortlist the top 25% of ideas, benchmarked against real peer-rated data 
from a corporate deliberation exercise (EDF).

**Key finding:** Simple pairwise LLM comparison recovered two-thirds of 
the top-rated ideas (Recall@25% = 0.667), outperforming a trained 
quality-attributes classifier (0.35) and direct prompting (0.43–0.49).
The classifier underperformed on real data because it over-relied on 
idea length, a finding we call the "length trap."

---

## Methods compared

| Method | Family | Recall@25% (EDF) |
|---|---|---|
| Pairwise Dynamic Rubric | Comparative | **0.667** |
| + Arguments (A2) | Direct prompting | 0.489 |
| + Q&A (A3) | Direct prompting | 0.456 |
| Bare (A1) | Direct prompting | 0.433 |
| Quality-attributes classifier | Classifier | 0.350 |
| Two-Ways AHP | Comparative | 0.330 |
| Random baseline | — | 0.250 |

---

## Repository structure
- notebooks/       : one notebook per method, numbered in order
- data/            : data description (real EDF data not included; see note)
- results/         : summary of outputs; full results in the thesis

---

## Data

The real dataset (EDF, 95 ideas, 4 themes) is proprietary and cannot be 
shared publicly. The synthetic training pool (2,395 ideas, 6 domains) was also 
generated using an LLM.

If you want to reproduce the work on your own data, any CSV with columns 
`idea_id`, `idea_text`, and `theme` will work as a drop-in replacement.

---

## Setup

All notebooks were built and run in Google Colab.  
To run locally, install the dependencies:

```bash
pip install -r requirements.txt
```

The LLM calls use the Google Gemini API. Set your API key as an 
environment variable before running:

```bash
export GEMINI_API_KEY="your_key_here"
```

---

## License

MIT License — free to use and adapt with attribution.
