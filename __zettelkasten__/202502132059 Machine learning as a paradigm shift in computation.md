---
tags:
  - "#machine-learning"
  - "#deep-learning"
  - "#math"
source: "[[Math and Architectures of Deep Learning]]"
Date: 2025-02-13
---
#### Machine learning
- Predictions are fundamental for life. To predict inputs (sensorial or knowledge) are necessary.
- Machine learning is a paradigm shift because we do not provide a step-by-step program, but instead we develop a mathematical model for the problem.
#### Classification
- When output is one of a set of possibilities, that's called a ***Classification problem***.
- Example:
	- A cat sees something, then based on that he can
		- Run away
		- Ignore
		- Approach
#### Quantitative estimations
- When output is not a within a set, is called a ***quantitative estimation***.
- Examples:
	- How long a lion must jump to reach its prey.
	- What would the temperature will be tomorrow at 3pm.
- Machines that make quantitative estimations are called #regressors.
#### Quantitative -> Classification
- Sometimes classifications outputs can be generated from quantitative estimations.
#### Model training
- Model training is done by multiplication of each input with a *weight* value + some bias value.
- Example:
	- When a cat sees an object.
		- If it's sharp(`s`) or hard(`h`) enough, should avoid it.
		- $$ y(s, h) = s\times{w_0} + s\times{w_1} + bias $$
- Weights are not know at first, we need to estimate it. This is called #Model-Training.
- The process of training follows these steps:
	1. Design a model with unknown parameters. ( #model-architecture)
	2. We estimate the optimal weights for the expected output via model training.
	3. Once the model is estimated, we can use the model to process real-life inputs an emits outputs. This is called #inferencing.
#### Model training process
- The most popular variety of machine learning is called **Supervised Learning**.
- In this variety, we:
	1. We provide inputs and random weight values.
	2. We generate the output.
	3. Compare that real output and adjust weights to make the output closer to the expected output.
	4. Repeat.
	5. After many attempts, we end up with weight values that approach their ideal values.
- This process is called ***training*** or ***learning***.
- The closer the distribution of training data is to real-life, the more likely the model performs better on real use cases.