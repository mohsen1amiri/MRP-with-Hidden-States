# **MRP-with-Hidden-States**
## On the Convergence of TD-Learning on Markov Reward Processes with Hidden States
This MATLAB code generates the transition matrices of hidden and observable states in two modes. In the first mode, both of matrices are generated randomly, and in the second mode the predefined matrices that are utilized in the paper are generated. At the end, the stationary distribution of both matrices are calculated.

Here is the variables that are employed in the code:

- dim_O: Dimention of the observable transition matrix (The number of observable states): dim\_O $\times$  dim\_O.
- dim_H: Dimention of the hidden transition matrix (The number of hidden states): dim\_H $\times$  dim\_H. 
- matrix_generation: If matrix_generation = ture, new transition probability matrices will be generated. If matrix_generation = false, the predifined transition probability matrices utilized in the paper will be generated.
- Vect_O: Initialized vector for the observable transition probability matrix generation. Note that, by changing the 'dim_O', this vector must be changed manually in a way that the number of the elements become 'dim_O' and the summation of the become 100.
- Vect_H: Initialized vector for the hidden transition probability matrix generation. Note that, by changing the 'dim_H', this vector must be changed manually in a way that the number of the elements become 'dim_H' and the summation of the become 100.
- P_O: The observable transition matrix.
- P_H: The hidden transition matrix.
- pi_O: The stationary distribution of observable states.
- pi_H: The stationary distribution of hidden states.

### The process of transition matrix generation
By having the 'Vect_O' or 'Vect_H', the first row of the matrix is created by this vector. Then, the new rows are created by using the random premutation of this vector.

### The process of stationary distribution calculation
By Perron-Frobenius theorem, the spectral radius of a transition matrix 'P' is 1. Therefore, we have: $P\nu=\lambda\nu$. Since the eigenvalue $\lambda$ could be 1 due to the Perron-Frobenius theorem, the eigenvector $\nu$ corresponds to $\lambda=1$ could be a good candidate for being a stationary distribution of 'P'. As a result, the stationary distribution is $\pi=\frac{\nu}{\sum_{i} \nu(i)}$.
