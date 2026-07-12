# Data

## Real dataset (EDF)
The EDF dataset (95 ideas, 4 themes, ~54 peer ratings per idea) was 
provided under a confidentiality agreement and cannot be shared publicly.

To use your own data, prepare a CSV with these columns:
- `idea_id` — unique identifier
- `idea_text` — the full idea content  
- `theme` — the discussion theme it belongs to
- `mean_rating` — average peer rating (for evaluation only)

## Synthetic dataset

The 2,395-idea synthetic training pool was generated using Claude AI 
(Anthropic) through structured prompting — not programmatically.

The generation process:
- 6 domains: Agriculture, Clean Water, Cybersecurity, Medical, 
  Smart City, and High School
- Approximately 400 ideas per domain
- Each idea was prompted to vary across quality dimensions 
  (relevance, workability, completeness, etc.) to produce a 
  realistic mix of strong and weak ideas

The prompt templates used for generation are documented in 
Appendix A of the thesis.

The synthetic dataset itself is not included in this repository 
because it was used solely for classifier training and does not 
constitute original collected data.
