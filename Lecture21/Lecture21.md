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
