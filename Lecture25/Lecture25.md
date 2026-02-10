# Lecture 25

---

## Normalization

- Technique applied for data preparation in ML.
- Change values of numeric columns in the dataset to a common scale, without distorting differences in the ranges of values.
- Scaling Techniques:
  - Min-Max Scaling
  - Mean Normalization
  - Max Absolute Scaling
  - Robust Scaling

### MinMax Scaling

- Need to find the maximum and minimum values of the data.
- Formula: $$ x*{\text{normalized}} = \frac{x - x*{\min}}{x*{\max} - x*{\min}} $$
- Geometrically, the dataset distribution will be fitting in a cube for 3D space, and rectangle/square for 2D space.

- Steps to apply MinMax Scaling:
  1. Find the minimum and maximum values of the dataset.
  2. Apply the formula to each value in the dataset.
  3. Split the dataset into training and testing sets.
  4. Train the model on the normalized training data.
  5. Evaluate the model on the normalized testing data.
  - IMP: Minimum value = 0, Maximum value = 1 after normalization.
  
### Mean Normalization
- Formula: $$ x*{\text{normalized}} = \frac{x - \mu}{x*{\max} - x*{\min}} $$
- Where $\mu$ is the mean of the dataset.
- Range of values after normalization: -1 to 1.
- If value is less than the mean, it will be negative; if greater than the mean, it will be positive.
- Rarely, but used for centering the data around zero.

### Max Absolute Scaling
- Formula: $$ x*{\text{normalized}} = \frac{x}{|x*{\max}|} $$
- Scales the data to the range [-1, 1] by dividing each value by the maximum absolute value in the dataset.
- Used in sparse data, where the data contains many zero values.

### Robust Scaling
- Formula: $$ x*{\text{normalized}} = \frac{x - \text{median}}{\text{IQR}} $$
- Where IQR (Interquartile Range) = Q3 - Q1.
- Robust to outliers, as it uses the median and IQR instead of mean and standard deviation.

### Normalization vs Standardization
- Requirement of feature scaling depends on the algorithm being used.
- Normalization is used when the distribution of data is not Gaussian and the algorithm does not assume any distribution.
- Standardization is used when the distribution of data is Gaussian and the algorithm assumes a normal distribution.

