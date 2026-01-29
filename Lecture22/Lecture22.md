# Lecture 22

---

## Pandas Profiling

- Pandas Profiling is a powerful tool for performing exploratory data analysis (EDA) on a DataFrame with just a single line of code.
- It generates a comprehensive report that includes various statistics and visualizations for each column in the DataFrame.
- To use Pandas Profiling, you need to install the `pandas-profiling` package if you haven't already:

```
pip install pandas-profiling
```

- It can generate a profile report as follows:

```
import pandas as pd
from pandas_profiling import ProfileReport
prof = ProfileReport(df)
prof.to_file(output_file="output.html")
```

- There are five sections in the Pandas Profiling report:
  1. Overview --> It shows general information about the DataFrame such as number of variables, observations, missing cells, and memory usage.
  2. Variables --> It provides detailed statistics for each variable including type, unique values, mean, median, standard deviation, and visualizations like histograms and box plots.
  3. Interactions --> It displays pairwise relationships between variables using scatter plots and correlation matrices.
  4. Correlations --> It shows correlation coefficients between numerical variables using different methods such as Pearson, Spearman, and Kendall.
  5. Missing Values --> It provides insights into the missing data patterns in the DataFrame using heatmaps and bar plots.

- Pandas Profiling helps in automating the entire EDA process that saves time and effort while providing valuable insights into the dataset.
