# Engineering ground-truth in Mathematics
### 1. Topic:
Mathematics

### 2. Background:
Nowadays, AI researchers are focused on solving math olympiad questions, which are assessed on benchmarks such as AIME problems, or even simpler problems such as GSM8K. Conveniently, these problems have ground-truth solution labels, making model training fairly accessible. However, mathematics is not defined by problems with clear-cut answers, not maths research anyways.

### 3. Research Question:
Can we develop better ground-truth labels/verifiers in other domains of mathematics, e.g. theorem proving?

### 4. Expected work:
Synthetic Data Generation: To create synthetic reasoning data, one can generate samples from the Bayesian network. A simple way to do this is by forward sampling: start by sampling values for the root nodes (nodes without parents), then proceed in topological order to sample values for the rest of the nodes given the values of their parents.

Understanding the Problem Statement: The model might struggle with parsing complex mathematical language, understanding the relationships between different quantities, or identifying what it's being asked to solve.

Identifying the Relevant Mathematical Concepts: The model might find it difficult to identify which mathematical concepts or principles apply to a given problem, especially if it involves abstract or advanced mathematics.

Formulating a Solution Strategy: The model might struggle to devise a plan or strategy for solving the problem, especially if it requires multiple steps or the application of multiple mathematical concepts.

Performing Calculations: While models typically excel at performing simple calculations, they might struggle with more complex ones, especially if they involve large numbers, fractions, or advanced mathematical functions.

Checking and Verifying the Solution: The model might find it difficult to verify whether its solution is correct, especially if this requires additional reasoning or calculation.

By examining the reward function, you could get insights into which of these stages the model is finding easy or difficult. For example, if the reward is high when the model correctly identifies the relevant mathematical concepts but low when it attempts to formulate a solution strategy, this could suggest that the model understands the problem well but struggles to devise a plan to solve it.
