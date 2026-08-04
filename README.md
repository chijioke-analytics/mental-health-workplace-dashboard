# Mental Health & Workplace Culture Dashboard

A Power BI dashboard exploring attitudes toward mental health in the tech industry, built from the Open Sourcing Mental Illness (OSMI) Mental Health in Tech Survey (1,259 respondents). The analysis focuses on how open people are about mental health at work, and whether the workplace environment affects that openness.

## Tools Used
- **Excel** — data cleaning
- **Power BI Desktop** — data modeling, DAX measures, visualization

## Data Cleaning (Excel)
The raw survey export had several data quality issues that needed fixing before analysis:
- Removed `Timestamp`, `state`, and `comments` columns — not relevant to the analysis
- Removed 8 rows with invalid data (raw `Age` values ranged from -1726 to 99999999999)
- Fixed a date-corruption bug in `no employees`, where Excel had auto-converted range labels like "1-5" and "6-25" into date text ("5-Jan," "25-Jun")
- Consolidated `Gender` from 49 inconsistent free-text entries (e.g. "cis male," "Trans woman," "msle") down to 4 categories: Female, Male, Others, Unknown
- Added two derived columns — `Age groups` (Early/Mid/Senior Career) and `Region` (mapped from Country) — to support demographic breakdowns

## Dashboard Pages

**Page 1 — Overview**
- Treatment rate by age group
- Family history rate by age group
- Work interference distribution
- Regional breakdown and tech-company employment split

**Page 2 — Openness & Stigma**
- Willingness to disclose mental vs. physical health issues in a job interview
- Comfort discussing mental health with coworkers vs. supervisors
- Employer's perceived treatment of mental vs. physical health
- Observed negative consequences for disclosing

## Key Finding
Respondents are far more comfortable discussing mental health with coworkers or supervisors than they are willing to disclose it in a job interview — and mental health interview disclosure lags well behind physical health interview disclosure. This gap points to a real disconnect between private openness and professional-context stigma.

## Files
- `mental Health survey.pbix` — Power BI file (open in Power BI Desktop to explore interactively)
- `survey.csv better.xlsx` — cleaned dataset
- Dashboard screenshots / PDF export — for a quick preview without opening Power BI

## Data Source
Open Sourcing Mental Illness (OSMI) Mental Health in Tech Survey
