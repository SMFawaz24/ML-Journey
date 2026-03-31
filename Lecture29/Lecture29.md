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

### How to Create a Pipeline

- Import the necessary libraries and classes.
- Define the steps of the pipeline as a list of tuples, where each tuple contains a name for the step and the corresponding transformer or estimator.
- Create an instance of the Pipeline class with the defined steps.
- Fit the pipeline on the training data using the `fit` method.

### Pipeline VS make_pipeline

- Pipeline requires you to name each step, while make_pipeline automatically assigns names based on the class names of the transformers and estimators.
- Pipeline allows for more flexibility in naming and ordering of steps, while make_pipeline is a simpler way to create a pipeline without worrying about naming the steps.
- Same can be said for ColumnTransformer and make_column_transformer.

### Exploring Pipelines

- We can explore the steps of a pipeline using the `named_steps` attribute, which returns a dictionary of the steps in the pipeline.

```python
print(pipeline.named_steps)
```

- We can also access individual steps of the pipeline using their names. For example, to access the imputer step, we can use:

```python
imputer = pipeline.named_steps['imputer']
```

- This allows us to inspect the parameters and attributes of each step in the pipeline, which can be useful for debugging and understanding the transformations being applied to the data.

- Pipelines can be tested with `accuracy_score` and `classification_report` to evaluate the performance of the model on the test data.

```python
from sklearn.metrics import accuracy_score, classification_report
y_pred = pipeline.predict(X_test)
print(accuracy_score(y_test, y_pred))
print(classification_report(y_test, y_pred))
```

### Cross-Validation with Pipelines

- Train and test of pipelines can be done multiple times using cross-validation to get a better estimate of the model's performance on unseen data.

```python
from sklearn.model_selection import cross_val_score
scores = cross_val_score(pipeline, X, y, cv=5)
print(scores)
```

### Exporting Pipelines

- Pipelines can be used in production by exporting them using `pickle`.
- This allows us to save the entire pipeline, including all the transformations and the trained model, and load it later for making predictions on new data.

```python
import pickle
with open('pipeline.pkl', 'wb') as f:
    pickle.dump(pipeline, f)
with open('pipeline.pkl', 'rb') as f:
    loaded_pipeline = pickle.load(f)
```
