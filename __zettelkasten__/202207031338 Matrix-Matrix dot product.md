# Matrix-Matrix dot product
---
- Apply vector-vector dot product to each row in A vs each column in B.
- The number of rows in the matrix A must be the the same as the columns in the matrix B.
- Example:
```python
[[1, 2],   [[5, 6],
 [3, 4]] .  [7, 8]]
= 
[ 
  [ [1,2].[5,7], [1,2].[6,8] ],
  [ [3,4].[5,7], [3,4].[6,8] ] 
]
= 
[
  [ (1*5 + 2*7), (1*6 + 2*8) ],
  [ (3*5 + 4*7), (3*6 + 4*8) ]
]
=
[
  [ ( 5 + 14), ( 6 + 16) ],
  [ (15 + 28), (18 + 32) ],
]
=
[
  [ 19, 22 ],
  [ 43, 50 ]
]
```

---
- Source: [[Deep learning]]
- Date: 2022-07-03
- Tags: #deep-learning #machine-learning #algebra #tensors #vectors #matrices  #dot-product
- See also:
	- [[202207031325 Vector-Vector dot product]]
	- [[202207031330 Vector-matrix dot product]]