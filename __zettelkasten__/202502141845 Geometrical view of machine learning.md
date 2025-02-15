---
tags:
  - machine-learning
  - AI
  - math
  - geometry
  - neural-networks
  - sigmoid
source: "[[Math and Architectures of Deep Learning]]"
Date: 2025-02-14
---

#### Machine learning as geometric concepts
##### Inputs
- Each input to a model is an array that can have $n$ dimensions. You can think of it as a point in high-dimensional space.
- The input space is often called *feature space*.
##### Outputs
- Each output is also a point in a high dimensional space.
- This output space is usually way smaller than the input space.
##### Machine learning
- A model maps a feature space point to an output space point.
- For classification jobs, we separate points into clusters in the output space which we use to determine categories.

#### 2D Space
- A good way to use the output score is to measure the distance from the line $x_0 + x_1 = 1$
![[CH01_F02_Chaudhury.png]]
- Here the distance can be determined as $$y = \frac{(x_0+x_1-1)}{\sqrt{2}}$$ Or in regular ML terms: $$y_(x_0, x_1) = \frac{1}{\sqrt{2}}x_0 + \frac{1}{\sqrt{2}}x_1 - \frac{1}{\sqrt{2}} $$
- This distance allows us to set thresholds based on the distance to the middle line. (like: close to -1, close to 0, close to 1)

#### Regression vs Classification
- There are two types of machine learning models: regressors and classifiers.
- Regressors generate a score prediction.
- Classifiers generate a class out of a set of predefined classes.
- We can convert a regressor into a classifier using thresholds.

#### Linear vs non-linear
- While some problems can be classified using a single line, most real-world problems aren't like that.
- Non-linear functions usually perform better.
- A very popular way to make inputs into non-linear values is to use a #sigmoid function.
- Is called sigmoid because it resembles the letter S.
- It usually is represented as the letter $\sigma$ .
- Its output usually generates a value between 0 and 1 (never 0, or 1).
- It isn't a linear transformation but a non-linear escalation.
- This helps to produce non-linear inputs that can accommodate better to fit the data.
![[CH01_F05_Chaudhury.jpg]]

#### Multi-layers: Deep neural networks
- There's a limit to how much a single layer can learn.
- For more complex patterns, we need to add more layers.
- Having more layers allows the network to learn more complex patterns and considerate more features.
- The advantages is that it would be able to recognize and produce better patterns but having too many layers can be computationally expensive and lead to overfitting.
![[CH01_F07_Chaudhury.png]]

- The output for the layers is calculated like:
	- $$  h_0^{(0)} = \sigma (w_{00}^{(0)}x_0 + w_{01}^{(0)}x_1 + \ldots +  w_{0n}^{(0)}x_n )$$
	- $$h_1^{(0)} = \sigma (w_{10}^{(0)}x_0 + w_{11}^{(0)}x_1 + \ldots +  w_{1n}^{(0)}x_n )$$
	- $$h_{n_0}^{(0)} = \sigma (w_{n_00}^{(0)}x_0 + w_{n_01}^{(0)}x_1 + \ldots +  w_{n_0n}^{(0)}x_n )$$
