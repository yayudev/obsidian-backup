# Affine Transformations (Tensors)
----
- An affine transformation is the combination of a **linear transform** + a **translation**.
- It has the shape `w . x + b` . 
-  Representations:

![[affine-transform.png]]

- Applying multiple successive transform will always produce and affine transform. This allows for multiple Dense layers to be applied in neural networks.
- On the other hand, applying `n` just Dense layers is not efficient as it could be the same as just applying 1. 
- To make it better, we need to include an activation function, like ReLU.

![[affine-tranform-with-relu.png]]

---
- Source: [[Deep learning]]
- Date: 2022-07-03
- Tags: #relu #machine-learning #affine-transform #tensors #image-processing #algebra #neural-networks #dense-layers #matematicas 
- See also:
	- [[202207031439 Translation (Tensors)]]
	- [[202207031444 Rotation (Tensors)]]
	- [[202207031453 Scaling (Tensors)]]