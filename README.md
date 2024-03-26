# **MRP-with-Hidden-States**
## On the Convergence of TD-Learning on Markov Reward Processes with Hidden States
This Python code generates the dynamics for two examples that are mentioned in the paper and runs the TD learning algorithm for cost-to-go function calculation.

### The process of stationary distribution calculation
By Perron-Frobenius theorem, the spectral radius of a transition matrix 'P' is 1. Therefore, we have $P\nu=\lambda\nu$. Since the eigenvalue $\lambda$ could be one due to the Perron-Frobenius theorem, the eigenvector $\nu$ corresponding to $\lambda=1$ could be a good candidate for being a stationary distribution of 'P'. As a result, the stationary distribution is $\pi=\frac{\nu}{\sum_{i} \nu(i)}$. Besides, it is also possible to import the pre-calculated invariant distribution.
