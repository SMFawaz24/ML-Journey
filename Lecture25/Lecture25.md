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
