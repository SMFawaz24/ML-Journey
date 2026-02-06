# Lecture 24

---

## Feature Scaling

- Feature Scaling is a technique to standardize the range of independent variables or features of data.
- Some independent variables, if not scaled properly, can bring in problems to the model performance.
- Types:
  - Standardization (Z-score Normalization)
  - Min-Max Scaling (Normalization)

### Standardization (Z-score Normalization)

- Transforms data to have a mean of 0 and a standard deviation of 1.
- Formula:
  \[
  z = \frac{(X - \mu)}{\sigma}
  \]
  where \(X\) is the original value, \(\mu\) is the mean of the feature, and \(\sigma\) is the standard deviation of the feature.
- The mean and standard deviation are always 0 and 1 respectively after standardization.
- Standardization works on:
  - Mean Centering
  - Scaling by Standard Deviation
<img width="1145" height="501" alt="Screenshot 2026-02-04 235419" src="https://github.com/user-attachments/assets/4be42b8d-56f4-4369-9595-fd51f86c0c8c" />

#### Importance of Scaling
- Values are accurate when the features are scaled properly.
- There is no harm in scaling the features, but it can lead to better performance of the model.
- Outliers can affect the mean and standard deviation, which can lead to poor performance of the model.
- **When to use Standardization?**
  - K-Means
  - K-Nearest Neighbors
  - Principal Component Analysis (PCA)
  - Artificial Neural Networks
  - Gradient Descent based algorithms

- Algorithms like Decision Trees, Random Forests, and Gradient Boosting do not require feature scaling as they are based on the concept of splitting the data based on feature values.

