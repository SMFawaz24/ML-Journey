# Lecture 27

---

## One Hot Encoding

- One hot encoding is used to convert categorical variables into a format that can be provided to machine learning algorithms to improve predictions.
- String categorical variables are converted into numerical values using one hot encoding.
- For example, if we have a categorical variable "Color" with three categories: Red, Green, and Blue, one hot encoding will create three new binary columns: "Color_Red", "Color_Green", and "Color_Blue".

### Dummy Variable Trap

- The dummy variable trap occurs when one of the dummy variables can be predicted from the others, leading to multicollinearity in the model.
- Multicollinearity is a situation where two or more independent variables are highly correlated, which can cause issues in regression models.
- To avoid the dummy variable trap, we can drop one of the dummy variables.

- We can reduce the number of columns by using only the most frequent variables in the dataset, which can help to avoid the dummy variable trap and improve model performance.

```pandas
pd.get_dummies(df,columns=['column1', 'column2'])
```

```
pd.get_dummies(df,columns=['column1', 'column2'], drop_first=True)
# This will drop the first category of each column, thus avoiding the dummy variable trap.
```
