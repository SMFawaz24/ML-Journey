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

### Without Pipelines vs With Pipelines

- Without pipelines, we would have to manually fit and transform the training data for each step, and then apply the same transformations to the test data. This can be error-prone and time-consuming.
- With pipelines, we can fit the entire pipeline on the training data and then use the same pipeline to transform the test data, ensuring that the same transformations are applied consistently.

### Pickling Pipelines

- We can also save and load pipelines using the `pickle` module in Python. This allows us to save the entire pipeline, including all the transformations and the trained model, and load it later for making predictions on new data.

### Strategies for Building Pipelines

- **Step 1:** Handle Missing Values
- **Step 2:** Apply OneHotEncoding for categorical features
- **Step 3:** Scale numerical features
- **Step 4:** Perform Feature Selection
- **Step 5:** Train Model (Decision Tree, Random Forest, Logistic Regression, etc.)

