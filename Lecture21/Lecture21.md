# Lecture 21

---

## Bivariate Analysis/Multivariate Analysis

- Bivariate analysis involves the examination of the relationship between two variables.
- Multivariate analysis extends this concept to more than two variables.
- It helps to understand how one variable affects or is associated with another variable.
- Can be used for different data combinations: numerical-numerical, numerical-categorical, and categorical-categorical.

- **Scatterplot** is used for numerical-numerical data.
- Example:

```
sns.scatterplot(tips['total_bill'], tips['tip'], hue=df['sex'], style=df['smoker'])
# Scatterplot for numerical-numerical data
```

- **Barplot** is used for numerical-categorical data.
- Example:

```
sns.barplot(df['categorical_column'], df['numerical_column'], hue=df['another_categorical_column'])
# Barplot for numerical-categorical data
```

- **Boxplot** is also used for numerical-categorical data.
- Example:

```
sns.boxplot(df['categorical_column'], df['numerical_column'], hue=df['another_categorical_column'])
# Boxplot for numerical-categorical data
```

- **Displot** is used for numerical-categorical data.
- Example:

```
sns.displot(df[df['categorical_column']=='category1']['numerical_column'], color='blue', hist=False)
sns.displot(df[df['categorical_column']=='category2']['numerical_column'], color='orange', hist=False)
# Displot for numerical-categorical data
```

- **Heatmap** is used for categorical-categorical data.
- Example:

```
sns.heatmap(pd.crosstab(df['categorical_column1'], df['categorical_column2']))
df.groupby(['categorical_column1']).mean()['categorical_column2']*100.plot(kind='heatmap')
# Heatmap for categorical-categorical data
```

- **Clustermap** is another option for categorical-categorical data.
- Example:

```
sns.clustermap(pd.crosstab(df['categorical_column1'], df['categorical_column2']))
# Clustermap for categorical-categorical data
```
