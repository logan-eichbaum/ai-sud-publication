# AI & Substance Use Disorder: Data-Driven Publishing Strategy

## Summary
This project applies data analytics and machine learning to a real-world research decision:  
**where should AI + Substance Use Disorder (SUD) research be published to maximize visibility and impact?**

Using publication metadata, citation patterns, and quality indicators, we built a framework to rank and recommend publishing venues that balance reach, credibility, and relevance.

---

## Problem
Researchers face growing pressure to publish in venues that:
- Maximize citations and visibility
- Maintain credibility and peer-review standards
- Reach the correct audience (researchers, clinicians, policymakers)

Selecting a publishing venue is often subjective. This project reframes it as a **data-driven decision problem**.

---

## Data
- **428 research articles**
- **240 publishing venues**
- Sources: Scrape Scholar + DOI-based metadata enrichment

**Key features**
- Citation count
- Publication year
- Venue
- Document type
- Reference count
- Quality indicators (methodology, clarity, transparency, relevance)

---

## Approach
- Enriched missing venue data using DOI metadata (Crossref, DataCite, OpenAlex, Elsevier)
- Cleaned and standardized records using **KNIME**
- Removed duplicates and structurally missing data
- Mitigated citation outliers via categorical feature engineering
- Aggregated data by venue, year, and document type
- Evaluated venues using multi-criteria ranking models

---

## Key Insights
- Citation impact is highly skewed by a small number of outliers
- High-impact venues often publish very few AI + SUD articles
- Recent-publication bias significantly affects citation metrics
- Venue quality cannot be assessed using citations alone

---

## Impact
This framework enables:
- More strategic publishing decisions
- Improved research visibility
- Ethical and interpretable evaluation of publication venues

The approach is transferable to **any domain where publication strategy matters**.

---

## Tools
- Python (PDF parsing, metadata extraction)
- KNIME (data cleaning and feature engineering)
- Scrape Scholar
- Excel
