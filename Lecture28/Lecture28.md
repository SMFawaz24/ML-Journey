# Lecture 28

---

## Column Transformer in Scikit-learn

- Column Transformer allows us to apply different transformations to different columns of a dataset.
- It is useful when we have a mix of numerical and categorical features in our dataset.
- It is a solution to the problem of applying different preprocessing steps to different types of data.
- We can use Column Transformer to apply one-hot encoding to categorical features and scaling to numerical features in a single step.
- It helps in building a more efficient and cleaner machine learning pipeline.
- Sparse matrices can be used with Column Transformer, which can save memory and computational resources when dealing with large datasets.

```python
from sklearn.compose import ColumnTransformer
transformer = ColumnTransformer(
    transformers=[
        ('tnf1', SimpleImputer(),['Fever']),
        ('tnf2', OneHotEncoder(),['Cough']),
        ('tnf3', OrdinalEncoder(),['Age'])
    ], remainder='passthrough')
transformer.fit_transform(df)
# This will apply SimpleImputer to the 'Fever' column, OneHotEncoder to the 'Cough' column, and OrdinalEncoder to the 'Age' column. The 'remainder' parameter will keep the other columns unchanged.
```
