# env-setup
A repository to store standardized workflow setup for data science and bioinformatics projects

## Essential Packages for Data Analysis 
```R
# 📌 Core packages for data wrangling and visualization
install.packages(c(
  "tidyverse",     # Includes dplyr, ggplot2, readr, tibble, etc.
  "readxl",        # Read Excel files
  "janitor",       # Clean column names and tables
  "skimr",         # Quick data summaries
  "here",          # File path management
  "tidyplots"      # Generate publication-ready plots for scientific papers
  "patchwork",     # Combine ggplots
  "plotly"         # Interactive plots
))
```
```R
# 📊 Table and summary reporting
install.packages(c(
  "gtsummary",     # Summary tables for clinical-style reports
  "gt"             # Table formatting engine used by gtsummary
))
```

```R
# 🧠 Easystats ecosystem (modeling, diagnostics, interpretation)
install.packages("easystats")  # Meta-package that includes:
# - insight
# - parameters
# - performance
# - report
# - effectsize
# - bayestestR
# - see
# - modelbased
```

```R
# ✅ Optional (recommended for statistical modeling workflows)
install.packages(c(
  "broom",         # Tidy up model outputs
  "car",           # Companion to Applied Regression
  "MASS"           # Core statistical functions and data
))
```



