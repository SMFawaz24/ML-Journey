# Lecture 29

---

## Machine Learning Pipelines in Scikit-learn

- A machine learning pipeline is a way to streamline the process of building a machine learning model by chaining together multiple steps, such as data preprocessing, feature selection, and model training.
- Scikit-learn provides a Pipeline class that allows us to create a pipeline of transformations and estimators.
- The Pipeline class takes a list of tuples, where each tuple contains a name for the step and the corresponding transformer or estimator.

```python
from sklearn.pipeline import Pipeline
pipeline = Pipeline(steps=[
    ('imputer', SimpleImputer()),
    ('encoder', OneHotEncoder()),
    ('scaler', StandardScaler()),
    ('model', LogisticRegression())
])
pipeline.fit(X_train, y_train)
# This will create a pipeline that first imputes missing values, then applies one-hot encoding, scales the features, and finally fits a logistic regression model.
```

- Pipelines chain together multiple steps so that the output of each step is used as input to the next step.
- Pipelines make it easy to apply the same preprocessing to train and test.
- Pipelines also help to avoid data leakage by ensuring that the transformations are only fit on the training data and then applied to the test data.
