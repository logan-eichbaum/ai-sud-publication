# AI & Substance Use Disorder: Data-Driven Publishing Strategy

## Summary
This project reframes academic publishing as a **data-driven decision problem**.  
Using metadata from AI + Substance Use Disorder (SUD) research, I built and evaluated multiple machine learning models to identify which publishing venues are most likely to yield **high citation visibility**.

The outcome is a reproducible framework for recommending publication venues while explicitly accounting for **temporal bias, outliers, and methodological limitations**.

---

## Business Problem
Researchers must choose where to publish under uncertainty:
- Citations accrue unevenly over time
- A small number of papers dominate visibility
- Venue reputation interacts with article type, timing, and quality

This project answers:
**Which journals are most likely to maximize visibility for AI + SUD research?**

---

## Data
- **311 cleaned articles** across **240 venues**
- Sources: Scrape Scholar + DOI metadata enrichment
- Features include:
  - Citation counts
  - References
  - Publication year
  - Document type
  - Venue
  - Quality indicators (relevance, clarity, transparency, methodology)

---

## Data Engineering & Cleaning
Tools: **KNIME + Python**

Key steps:
- Removed duplicates and unknown venues
- Imputed or removed null values
- Created categorical ranges for citations and references to reduce temporal bias
- Normalized citations by years since publication
- Aggregated low-frequency venues to reduce sparsity

**Result:** Cleaner, more reliable dataset while acknowledging introduced biases.

---

## Modeling Approach
Three classification models were developed to predict citation impact (Low / Medium / High):

- **Multinomial Logistic Regression**  
  - Baseline, interpretable benchmark
- **Decision Trees (C5.0 / CART)**  
  - Capture non-linear interactions
- **Random Forest**  
  - Primary model for stability and performance

Validation strategy:
- Stratified 70/30 train-test split
- Nested cross-validation
- Bias controls for time, outliers, and venue sparsity

---

## Key Findings
Across all models:
- **Venue** is a strong predictor of citation visibility
- **Publication year** matters, but venue effects persist after temporal normalization
- **Online and open-access medical journals** consistently outperform others

**Top venues identified across models:**
- JAMA Network Open
- PLOS One
- Journal of the American Medical Informatics Association

---

## Impact
This project demonstrates how:
- Publishing strategy can be optimized using analytics
- Biases in real-world data can be identified and mitigated
- Model results can support **prescriptive recommendations**, not just predictions

The framework generalizes to **any research domain** where visibility and impact matter.

---

## Tools & Technologies
- Python (pandas, scikit-learn)
- KNIME
- Excel
- Data visualization & statistical testing
