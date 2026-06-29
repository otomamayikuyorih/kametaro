# Data004: AI adoption PLS-SEM demo

Source: Navara & Prabowo (2026), Mendeley Data, DOI https://doi.org/10.17632/fs78cfs84v.2

This folder contains the downloaded Excel file and a reproducible `lvsem` analysis that follows the same demo style as the other `PLS-SEM/demo` folders:

- `Excel data respondent.xlsx`: original downloaded Mendeley file
- `data004_ai_adoption_clean.csv`: renamed Likert indicators used in the model
- `Data_Dictionary.csv`: mapping from short indicator names to source columns
- `data004_analysis.Rmd`: reproducible R/lvsem analysis notebook
- `data004_analysis.html`: HTML report
- `data004_lvsem_ai_adoption_model.png`: structural model figure
- `data004_path_coefficients_bootstrap.csv`: path estimates with 1000 bootstrap standard errors
- `data004_reliability_ave.csv`: Cronbach alpha, composite reliability, and AVE
- `data004_outer_loadings.csv`: indicator loadings
- `data004_latent_scores.csv`: construct scores
- `data004_r2.csv`: endogenous construct R-squared values

Regenerate the report with:

```powershell
& 'C:\Program Files\R\R-4.4.0\bin\Rscript.exe' -e "rmarkdown::render('data004_analysis.Rmd')"
```

Note: the final seven manifest variables are treated as `Innovation_Capability` because this matches the dataset description and structural model. Their literal wording is decision-quality oriented, so construct interpretation should be checked against the authors' intended instrument.
