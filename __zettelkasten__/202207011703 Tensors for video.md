# Tensors for video

----

- Images are handled better using Rank-4 tensors (4D).
- Images need to store 4 dimmensions: 
	- Frames (usually `video's length * frame rate`)
	- Height
	- Width
	- Color depth (channels)
- Default format for image tensors is `(frames, height, width, color_depth)`.
- Common convention currently is *channels-last*, so color info is always the last dimmension in the tensor.

---
- Source: [[Deep learning]]
- Date: 2022-07-01
- Tags: #machine-learning  #AI  #deep-learning #tensors #images #image-processing
- See also: