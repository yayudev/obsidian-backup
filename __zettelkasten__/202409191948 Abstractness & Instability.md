# 202409191948 Abstractness & Instability
----
- Abstractness is the ratio of abstract artifacts (like interfaces) to concrete artifacts (classes, functions).
- Instability is the ratio of efferent coupling (outgoing) vs the total coupling (incoming + outgoing).
- Instability measures the volatility of the codebase. 
- Higher instability means that a change on that artifact may break the rest of the code since a lot of parts depend on it.

- Code that is too abstract is difficult to use  -- uselessness
- Code that is too concrete is easy to break and hard to maintain -- painful
- Thus, a good balance between abstraction and concreteness is required.

---
- Source: [[Fundamentals of Software Architecture]]
- Date: 2024-09-19
- Tags: #software #software-architecture 
- See also: