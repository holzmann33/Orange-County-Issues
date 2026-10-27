# Orange County Residents' Concerns, 1989 vs. 1994

A Python analysis comparing the two Orange County Annual Surveys: how residents'
top concerns changed, which groups were most concerned, and whether the survey
year still predicts concern after adjusting for demographics.

**Rendered notebook:** [PAGES LINK]

## What the notebook does
- Reads the original fixed-width survey files directly from the zipped data,
  using the column positions from the SPSS syntax files
- Harmonizes variables and response categories across the two surveys
  (age, education, income, party, region, gender, homeownership)
- Compares top concerns and financial outlook with survey weights
- Reports weighted crime concern by demographic group and year
- Tests whether demographic gaps changed between 1989 and 1994 using
  interaction models
- Estimates the year effect on concern with a logistic regression
  adjusted for demographics

## Key finding
Crime rose from about 11% of respondents' top concern in 1989 to about 31% in
1994. The 1994 coefficient stays strongly significant after controlling for
demographics (odds ratio about 3.5).

## Data comparability note
The 1989 public-policy question had no "economy" response option, so crime is
compared directly as a top concern, while economic attitudes are compared using
the financial-outlook questions both surveys shared.

## Data
Orange County Annual Surveys, 1989 and 1994
(DOIs: 10.7280/D1KW29 and 10.7280/D1Z594).
[Note here whether the data files are included in this folder or must be
downloaded from the DOI links above.]

## Reproducing
Install the packages in the root `requirements.txt`, place the two `.zip` data
files in this folder, and run the notebook from top to bottom.

**Tools:** Python, pandas, NumPy, statsmodels, matplotlib
