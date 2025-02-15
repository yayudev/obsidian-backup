---
tags:
  - math
  - matrices
  - vectors
  - machine-learning
source: "[[Math and Architectures of Deep Learning]]"
Date: 2025-02-15
---
#### Matrices
- A matrix can be viewed as a rectangular array of numbers with fixed number of rows and columns.
- A matrix can also be seen as a collection of row vectors.
- Example: $$x =
\begin{bmatrix}
	0.11 & 0.09 \\
	0.01 & 0.02 \\
	0.98 & 0.91 \\
	0.12 & 0.21 \\
	0.98 & 0.99 \\
	0.85 & 0.87 \\
	0.03 & 0.14 \\
	0.55 & 0.45 
\end{bmatrix}
$$
#### Matrices to represent digital images
- Digital images are often represented using matrices.
- And example would be a grayscale image:
	- Assuming that each element is a pixel.
	- The value of each pixel represents the brightness for that pixel (0-255)
	- Example: $$
\begin{bmatrix}
	0   & 8   & 16  & 24  & 32  & 40  & 48  & 56  & 64  \\
	64  & 72  & 80  & 88  & 96  & 104 & 112 & 120 & 128 \\
	128 & 136 & 144 & 152 & 160 & 168 & 176 & 184 & 192 \\
	192 & 200 & 208 & 216 & 224 & 232 & 240 & 248 & 255 \\
\end{bmatrix}
$$
### Matrices in PyTorch
- You can think of tensors as multidimensional arrays.
	- Scalars are 0D tensors.
	- Vectors are 1D tensors.
	- Matrices are 2D tensors.

- Create a matrix:
```python
vector = torch.tensor(
	 [ # 2D Vector
		 [0.11, 0.01, 0.98, 0.12],
		 [0.15, 0.21, 0.34, 0.23],
		 [0.32, 0.53, 0.84, 0.90],
	 ], 
	 dtype=torch.float64,  # 64bit floats 
 ) 
```
- Accessing elements
```python
first_element = matrix[0]
last_element = matrix[-1, 0]

second_to_fifth_elements = vector[1:5]
```
