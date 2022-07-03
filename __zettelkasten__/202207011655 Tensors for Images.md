# Tensors for images

----

- Images are handled better using Rank-3 tensors.
- Images need to store 3 dimmensions: 
	- Height
	- Width
	- Color depth (channels)
- Default format for image tensors is `(height, width, color_depth)`.
- Common convention currently is *channels-last*, so color info is always the last dimmension in the tensor.

---
- Source: [[Deep learning]]
- Date: 2022-07-01
- Tags: #machine-learning  #AI  #deep-learning #tensors #images #image-processing
- See also: