---
tags:
  - "#AI"
  - machine-learning
  - Model-Training
  - model-architecture
source: "[[Math and Architectures of Deep Learning]]"
Date: 2025-02-13
---
#### Inputs
- We usually want to normalize the inputs first.
- #normalization is a math trick where we take all possible values and transform them to values between 0 and 1.
- Math definition:
	- Given:  $$ v = input \space value $$
	- Then $$ v_{norm} = \frac{(v-v_{min})}{(v_{max} - v_{min})} $$
	- The result will then be: $$ \vec{x} = \begin{bmatrix} x_0 \\ x_1 \end{bmatrix} \in [0, 1]^2 $$
#### Outputs
- The final output is multi-class, meaning we have a set of possible output values.
- To convert from a quantitative value to a classification ($o$), we generate a *score* value ($y$) and a threshold ($\delta$).
- For example: 
	- Given that $y = calculated \space value$  and $\delta = score$ and $o \in [0, 1, 2]$: $$
\left
\{\begin{array}{l} 
	y \gt \delta & 0 \\
	-\delta \ \le \ y \le \delta & 1\\
	y \lt -\delta & 2 \\
\end{array} 
\right.
$$
#### Model estimation
- We want to generate a function that transforms the input vector into an ouput ( $y(\vec{x})$ ).
- We don't know that exact perfect function, so instead we try to estimate it.
- The steps to create that estimation are:
	1. *Model architecture selection* - Design a parametrized function that we expect would be a good proxy to the unknown ideal function.
	2. *Training* - Estimate the best parameters that would match the input to the outputs using the designed function.
#### Model architecture selection
- This differs between machine learning approaches.
- The simple model is using weight parameters ($w_0,w_1, \ldots, w_n$) to add weight to each input and a bias ($b$) constant special parameter that doesn't change.
- In math definition, parameters are: $$\vec{w} =\begin{bmatrix} w0 \\ w_1 \end{bmatrix} \in \mathbb{R}^2 $$
- Thus, given the inputs ($\vec{x}$): $$ y(\vec{x}) = b +\sum_{i=0}^n{(\vec{w_i}\times\vec{x_i})} $$
- So for 2 inputs ($x_0, x_1$): $$ 
y(x_0, x_1) = 
	\begin{bmatrix}
		w_0 & w_1
	\end{bmatrix}
	\begin{bmatrix}
		x_0 \\ x_1
	\end{bmatrix}
	+ b
	= \vec{w}^T\vec{x} + b
$$
#### Model training
- The goal of training is to find or estimate the parameters ($\vec{w}$) such that the generated the outputs ( $y_0, y_1$ ) with the training data inputs ( $x_0, x_1$ ) will match the expected outputs for each as much as possible (*GT/ Grounded Truth*).
- The problem of finding the right weights for a model is known as *function-fitting* problem in mathematics.
- Mathematicians usually use a closed-form solution where the parameters are estimated by solving equations that contain all the training data items together. That approach is not practical in real-life (due to memory concerns), so we instead use an iterative approach where we load small portions of data at a time.
##### Iterative approach
- In each iteration, we calculate the difference between the generated output ($y_{predicted}$) and the expected one ($y_{expected}$). The error for each prediction is calculated like $$
E^2 = (y_{predicted}^{(i)} - y_{expected}^{(i)})^2
$$
- The total error is calculated using $$
E^2 = \sum_{i=0}^N{(y_{predicted}^{(i)} - y_{expected}^{(i)})^2}
$$ On each iteration we want to reducer this total error.
- For the iterative approach we use this approach:
	**while ( $E^2 = \sum_{i=0}^N{((\vec{w}^T\vec{x}^{(i)} + b) - y_{expected}^{(i)})^2}$ ) do**
		**for ( $\forall_i \in [0, N]$ ) do**
			Adjust $\vec{w}$ so that $E^2$ is reduced.	
		**end for**
	**end while**
	
	The final parameters are the optimal values:$$
		\vec{w_*}\leftarrow \vec{w} \ , \ b_* \leftarrow b
	$$
#### Inferencing
- In real world we deploy the model with the optimal parameters ($\vec{w_*} \ ,\ b_*$).
- The new parameter will receive new inputs ( $\vec{x}$ ) and will infer using $$y_{predicted}(\vec{x}) = \vec{w_*}^T \vec{x} + b_*$$
