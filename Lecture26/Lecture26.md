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
