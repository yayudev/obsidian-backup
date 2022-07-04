# Scaling (Tensors)
----
- Scaling of a figure can be done using a dot product of a point or matrix vs the following 2x2 matrix:
```python
scaling_matrix = 
[
  [horizontal_factor,        0        ],
  [       0         , vertical_factor ]
]
```

- For example, to scale a figure 1.5x horizontal and 0.5x horizontal, we would use the dot product as it follows:
```python
# scale_matrix . [x, y]
[ [ 1.5,  0 ],
  [  0 , 0.5] ] . [x, y] # or against the image matrix 

``` 

- That would be represented as:

![[tensor-scale.png]]

---
- Source: [[Deep learning]]
- Date: 2022-07-03
- Tags: #deep-learning  #image-processing #algebra #matrices #dot-product #vectors #rotation #linear-transformations
- See also: