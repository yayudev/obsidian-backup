# Modularity - Measuring Modularity 
----
#### Cohesion
- Cohesion is to what extend the parts of a module should be contained within it.
- It refers to how much the parts are related to each other.
- Attempting to divide a cohesive module would only result in increased coupling and decreased readability.
- Some types are:
	- Functional - each part is related to each other
	- Sequential - one part's output is input to another
	- Procedural - two parts must execute in order
	- Communicational - One part notifies another.
	- Logical - Two parts are related to the same data, but no between them, like util modules.
	- Coincidental - both parts are just in the same file without any relation between them. This should be avoided.
- LCOM - Lack of COhesion in Methods
- LCOM is the sum of set of methods that don't share fields. See:
![[fosa_0301.png]]

#### Coupling 
- Theres two types of coupling:
	- *Afferent*: incoming connections to the module.
	- Efferent: outgoing connections from the module.

---
- Source: [[Fundamentals of Software Architecture]]
- Date: 2024-09-19
- Tags: #modularity #programming #software-development #software-architecture 
- See also: