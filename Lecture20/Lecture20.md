# Lecture 20

---

## Types of Data

- Numerical Data: Quantitative data that can be measured (e.g., height, weight).
- Categorical Data: Qualitative data that represents categories (e.g., gender, color).

## Univariate Analysis

- Univariate analysis involves the examination of a single variable.
- It helps to understand the distribution, central tendency, and variability of the data.
- Matplotlib and Seaborn are commonly used libraries for visualization.
- For categorical data, common visualizations include bar graphs and pie charts.
- Examples:
  - Total Count
  ```
  sns.countplot(df['categorical_column'])
  df['categorical_column'].value_counts().plot(kind='bar')
  # Bar graph for categorical data
  ```

  - Percentages
  ```
  df['categorical_column'].value_counts().plot(kind='pie', autopct='%.2f')
  # Pie chart for categorical data
  ```
- For numerical data, we use histograms, distplots and box plots.
- Examples:
  - Histogram
  ```
  plt.hist(df['numerical_column'], bins=30)
  # Histogram for numerical data
  ```

  - Distplot
  ```
  sns.distplot(df['numerical_column'], bins=30, kde=True)
  # KDE --> Kernel Density Estimation
  # Gives the probability density function of the variable
  ```

  - Box Plot
  ```
  sns.boxplot(df['numerical_column'])
  # Box plot for numerical data
  ```
- Calculating stats from data:

```
mean = df['numerical_column'].mean()
median = df['numerical_column'].median()
mode = df['numerical_column'].mode()[0]
std_dev = df['numerical_column'].std()
variance = df['numerical_column'].var()
min_value = df['numerical_column'].min()
max_value = df['numerical_column'].max()
range_value = max_value - min_value
skewness = df['numerical_column'].skew()
```

- Skewness checks the variablity of data
  - Positive Skew: Right tail is longer; mean > median
  - Negative Skew: Left tail is longer; mean < median
  - Symmetric: Mean = Median
