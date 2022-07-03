# Matrices (Tensors)
----

- Matrices are *Rank-2* tensors. 
- They are 2-D arrays of numbers.
- They are good for data that need to be aware of time.

Example:
- To analyze how stock prices change during the day we need the following current, Highest and Lowest price each minute. 
- We need to group every minute into a day representation.
- Then we would model that as the following tensor (2D array):

```js
	[
	// [current, highest, lowest]
		[10, 11, 9], // <- One minute
		[11, 12, 9], // <- One minute
	] // <- One day
```


---
- Source: [[Deep learning]]
- Date: 2022-07-01
- Tags: #machine-learning  #AI  #deep-learning  #tensors #numpy #python 
- See also: