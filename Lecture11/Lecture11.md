# Lecture 11

---

## Tensors

- Container for storing numbers.

### OD Tensors / Scalars

- Simple, tensors that only have 1 number stored. They have 0 dimensions.

### 1D Tensors / Vectors

- Tensors storing a 1-D array with multiple numbers have 1 dimension.
- Collection of scalars.
- Vectors have different dimensions than Tensors.
- Examples: Any ML data row

### 2D Tensors / Matrices

- Tensors storing multiply vectors form matrices.
- They have 2 dimensions (row, column).
- Examples: Collection of input columns of an ML data can be stored in a matrix.

### ND Tensors

- Greater Tensors can be created by collecting more matrices and higher structures to form 3D, 4D, 5D Tensors.

### Rank, Axis, Shape and Size

- No. of axis = Rank = No. of dimensions
- Shape = (dim1, dim2) (2D Tensors)
- Size = dim1 * dim2 (2D Tensors)

### 3D, 4D and 5D Tensors (Examples)

- All Time-series datasets - 3D Tensors
- Image Classification/Processing - 4D Tensors
- Collection of Videos / Video Processing - 5D Tensors
