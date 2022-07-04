# Rotation (Tensors)
----
- Counter-clock wise rotation of a figure in a `theta` angle can be done using a dot product of a vector or matrix vs the following 2x2 matrix:
```python
rotation_matrix = [
  [cos(theta), -sin(theta)],
  [sin(theta), cost(theta)]
] 
```

- Thus to rotate a point, we would use the dot product as it follows:
```
rotation_matrix . [x, y]
``` 

- That would be represented as:

![[tensor-rotation.png]]

---
- Source: [[Deep learning]]
- Date: 2022-07-03
- Tags: #deep-learning  #image-processing #algebra #matrices #dot-product #vectors #rotation #linear-transformations
- See also: