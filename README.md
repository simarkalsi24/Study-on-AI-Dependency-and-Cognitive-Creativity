# 🧠 Study on AI Dependency and Cognitive Creativity

A survey-based research dataset exploring how regular AI tool usage affects human creativity, cognitive effort, and self-perceived originality.

---

## Overview

This dataset was collected through a structured questionnaire administered to **100 real respondents** across varying age groups, genders, and educational backgrounds. The study investigates the relationship between AI dependency and core cognitive traits — particularly creative confidence and mental effort during unassisted tasks.

The dataset has been **statistically augmented to 5,000 rows** using empirical distribution sampling, preserving all real-world distributions and cross-column correlations from the original responses.

---

## Files

| File | Description |
|------|-------------|
| `Study_on_AI_Dependency_and_Cognitive_Creativity.csv` | Original 100 real survey responses |
| `Study_on_AI_Dependency_5000_v2.csv` | Augmented dataset (5,000 rows, statistically sampled) |

---

## Dataset Columns

| Column | Type | Description |
|--------|------|-------------|
| `Timestamp` | datetime | Time of survey submission |
| `Age` | integer | Respondent's age |
| `Gender` | categorical | Male / Female |
| `Educational Background` | categorical | High school or below / Undergraduate / Graduate / Postgraduate / PhD |
| `Do you regularly use AI tools?` | categorical | Yes / No |
| `If yes, how often?` | categorical | Rarely / A few times a week / Once a day / Multiple times a day |
| `What tasks do you use AI for?` | multi-select | Writing, Research, Coding, Brainstorming, etc. |
| `AI Dependency (1–5)` | integer | Self-rated dependency on AI tools (1 = not dependent, 5 = highly dependent) |
| `Open-ended paragraph` | free text | Written response to: *"If the internet disappeared tomorrow, how would your life change?"* — written without AI assistance to measure natural creativity |
| `Were you aware AI could generate write-ups?` | categorical | Yes / No |
| `How mentally tiring was the task?` | integer (1–10) | Self-rated cognitive effort during the writing task |
| `How confident are you in your originality?` | integer (1–10) | Self-rated confidence in the originality of their response |
| `Were you tempted to use AI while writing?` | categorical | Yes / No |
| `Do you feel AI has reduced your own creativity?` | categorical | Yes / No / Maybe |

---

## Key Statistics (Original 100 Responses)

**Demographics**
- Gender split: 50% Male, 50% Female
- Age range: 14–54 (mean ≈ 25)
- Largest group: Undergraduate students (53%)

**AI Usage**
- 88% use AI tools regularly
- 52% use AI multiple times a day
- Most common tasks: Research, Writing, Brainstorming, Coding

**Dependency & Creativity**
- Most common dependency score: **3 / 5** (48% of respondents)
- 44% were tempted to use AI mid-task even when asked not to
- Mean originality confidence: **7.9 / 10**
- Mean mental tiredness: **4.5 / 10**
- Respondents who resisted AI temptation rated their originality higher on average (**8.2 vs 7.6**)

---

## Augmentation Methodology

The original 100 responses were expanded to **5,000 rows** using **empirical distribution sampling** — a statistics-based approach that requires no external generative models.

**Key principles applied:**

- **Correlated generation** — columns were not sampled independently. Real-world dependencies were preserved:
  - Age was sampled conditioned on education level (e.g., undergrads aged 18–25, PhD respondents aged 30–55)
  - AI dependency was conditioned on usage frequency
  - Temptation to use AI was conditioned on dependency score
  - Mental tiredness was conditioned on dependency score
  - Originality confidence was conditioned on temptation response

- **NaN patterns preserved** — missingness rates were maintained per column

- **Free-text paragraphs** — resampled from the 100 real responses (no fabrication)

- **Casing normalized** — inconsistent responses (e.g., `yes` / `Yes` / `YES`) were standardized

No language models were used to generate synthetic text responses.

---

## Potential Use Cases

- Studying the relationship between AI usage frequency and creative self-efficacy
- NLP analysis of open-ended responses for creativity scoring
- Classification models predicting AI dependency from demographic data
- Benchmarking human-written paragraphs for originality detection
- Education research on AI's impact on student cognitive habits

---

## Limitations

- Original sample is small (n=100) and skewed toward younger, undergraduate respondents
- Self-reported measures are subject to social desirability bias
- The augmented dataset reflects patterns in the original sample — it does not introduce new demographic diversity
- Open-ended paragraphs in the augmented set are resampled from originals, not independently generated

---

## License

This dataset is shared for academic and research purposes. If you use it in your work, please cite or credit this repository.

---

## Contributing

Found an issue or want to extend the study? Open an issue or submit a pull request. Contributions to analysis notebooks, visualizations, or methodology improvements are welcome.
