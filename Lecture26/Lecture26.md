# Lecture 26

---

## Encoding Categorical Data

- Categorical data is non-numeric data that can be divided into categories or groups.
- Types of categorical data:
  - Nominal: No inherent order (e.g., colors, types of animals).
  - Ordinal: Has an inherent order (e.g., education level, customer feedback).
- Types of encoding techniques:
  - Ordinal Encoding
  - One-Hot Encoding
  - Label Encoding

### Label Encoding

- Assigns a unique integer to each category in the dataset.
- Suitable for ordinal data where the order of categories matters.
- Output is a single column with integer values representing the categories.
- Example:
  | Color | Label Encoding |
  |--------|----------------|
  | Red | 0 |
  | Green | 1 |
  | Blue | 2 |
- Example of using label encoding in a machine learning model:
  - If we have a dataset with a feature "Color" and we want to predict the type of fruit, we can use label encoding to represent the colors as integers. This allows the model to understand that different colors may be associated with different types of fruits.

### Ordinal Encoding

- Similar to label encoding but takes into account the order of categories.
- Assigns integer values based on the order of categories.
- Example:
  | Education Level | Ordinal Encoding |
  |-----------------|-----------------|
  | High School | 0 |
  | Bachelor's | 1 |
  | Master's | 2 |
  | PhD | 3 |

- Example of using ordinal encoding in a machine learning model:
  - If we have a dataset with a feature "Education Level" and we want to predict income, we can use ordinal encoding to represent the education levels as integers. This allows the model to understand that higher education levels may be associated with higher income.

- The order of the categories is important in ordinal encoding, and it can lead to better performance in certain machine learning algorithms that can take advantage of the order.
- However, it may not be suitable for nominal data where there is no inherent order.
- It can also lead to issues if the model assumes a linear relationship between the encoded values, which may not be the case for ordinal data.
- It is important to carefully consider the nature of the data and the requirements of the machine learning algorithm when choosing an encoding technique for categorical data.
