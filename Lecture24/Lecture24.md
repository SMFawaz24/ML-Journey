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

