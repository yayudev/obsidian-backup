# Tensor Reshaping
----
- Reshaping means changing the way the values in the tensor are organized to have the same data in a different shape.
- New shape must be able to hold the original number of values.
- Example:
```python
# Original tensor. Shape => (3, 2)
[
  [0, 1],
  [2, 3],
  [4, 5]
]

# Reshaping this to (6,)
[ 0, 1, 2, 3, 4, 5 ]

# Note that 3*2 = 6, so both can hold the same number of values
```

- One of the most common usages is: 
	- [[202207031419 Matrix Transposition]]

---
- Source: [[Deep learning]]
- Date: 2022-07-03
- Tags: #deep-learning #machine-learning #tensors #reshaping #algebra 
- See also: