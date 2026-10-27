# NAGALA Japanese cohort

`nagala.xlsx` is an unchanged copy of the original `Data set Int J Obesity.xlsx` (locally downloaded as `Data+set+Int+J+Obesity.xlsx`).

## Source and citation

Okamura, Takuro; Hashimoto, Yoshitaka; Hamaguchi, Masahide et al. (2019). Data from: Ectopic fat obesity presents the greatest risk for incident type 2 diabetes: a population-based longitudinal study [Dataset]. Dryad. https://doi.org/10.5061/dryad.8q0p192

Dataset version: February 19, 2019.
Related publication: https://doi.org/10.1038/s41366-018-0076-3
Dryad distributes research data under CC0. Source terms: https://datadryad.org/terms

## Load in a notebook

```python
import pandas as pd

url = "https://raw.githubusercontent.com/Ratul-34/Diabetes-Health-Indicators/main/data/nagala.xlsx"
df = pd.read_excel(url, sheet_name="Sheet 1", engine="openpyxl")
print(df.shape)
df.head()
```

If the Excel reader is missing, run `%pip install openpyxl` once in Jupyter.

The workbook contains 15,464 data rows and 31 columns. Column names, units, values, missing cells and ordering are preserved. It includes baseline predictors, participant numbers, derived obesity categories, follow-up duration in days and the outcome `Incident DM 0/1`.

For baseline prediction, keep participant numbers, follow-up duration and outcome separate from predictor features. Follow-up is needed to define the prediction horizon and handle censoring. Several measurements appear in two units; these are alternate representations, not independent predictors.
