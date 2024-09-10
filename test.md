# WEEK 1. NN Weight update

---

In neural networks, the weights of the connections between neurons are updated during training using gradient-based optimization techniques, with backpropagation being the most common approach. Here's the general process of updating weights in a neural network:

### 1. **Gradient Descent**
In its simplest form, weights are updated using the following formula:

$$\large
\textcolor{darkviolet}{
w_{new} = w_{old} - \eta \cdot \frac{\partial L}{\partial w}
}
$$

Where:
- $w_{new}$ is the updated weight,
- $w_{old}$ is the current weight,
- $\eta$ is the learning rate (a small positive value),
- $\frac{\partial L}{\partial w}$ is the gradient of the loss function $L$ with respect to the weight $w$.

### 2. **Backpropagation**
In a neural network, the loss $L$ is propagated back through the network, and the partial derivatives of the loss with respect to each weight are computed using the chain rule of calculus. This allows weights at each layer to be updated.

For each neuron $j$ in layer $l$, we calculate the gradient of the loss function with respect to its weight $w_{ij}^{(l)}$ connected to neuron $i$ from the previous layer $l-1$.

The weight update formula during backpropagation becomes:

$$\large
\textcolor{darkviolet}{
w_{ij}^{(l)} = w_{ij}^{(l)} - \eta \cdot \delta_j^{(l)} \cdot a_i^{(l-1)}
}
$$

Where:
- $\delta_j^{(l)}$ is the error term for neuron $j$ in layer $l$,
- $a_i^{(l-1)}$ is the activation of neuron $i$ from layer $l-1$,
- $\eta$ is the learning rate.

### 3. **Error Term Calculation ($\delta_j^{(l)}$)**
The error term $\delta_j^{(l)}$ is calculated differently for output and hidden layers:

- For output neurons:
  
  $$\large
  \textcolor{darkviolet}{
  \delta_j^{(output)} = (a_j^{(output)} - y_j) \cdot f'(z_j^{(output)})
  }
  $$
  
  where:
  - $a_j^{(output)}$ is the activation of the output neuron,
  - $y_j$ is the actual target value,
  - $f'(z_j^{(output)})$ is the derivative of the activation function applied to the pre-activation $z_j^{(output)}$.

- For hidden neurons:
  
  $$\large
  \textcolor{darkviolet}{
  \delta_j^{(l)} = \left( \sum_k \delta_k^{(l+1)} \cdot w_{jk}^{(l+1)} \right) \cdot f'(z_j^{(l)})
  }$$
    
  where:
  - The summation is over all neurons $k$ in the next layer $l+1$,
  - $w_{jk}^{(l+1)}$ is the weight connecting neuron $j$ in layer $l$ to neuron $k$ in layer $l+1$,
  - $f'(z_j^{(l)})$ is the derivative of the activation function for neuron $j$ in layer $l$.

### 4. **Variants of Gradient Descent**
- **Stochastic Gradient Descent (SGD)**: Weights are updated after every training example.
  
  $$\large
  \textcolor{darkviolet}{
  w_{new} = w_{old} - \eta \cdot \nabla L(w; x_i, y_i)
  }
  $$

- **Mini-Batch Gradient Descent**: Weights are updated after processing a batch of training examples.

- **Momentum**: Adds a velocity term to the update rule.
  
  $$v_t = \gamma v_{t-1} + \eta \cdot \frac{\partial L}{\partial w}$$
  
  $$w_{new} = w_{old} - v_t$$
  where $v_t$ is the velocity at time step $t$, and $\gamma$ is the momentum coefficient.
  
- **Adam Optimizer**: Combines momentum and adaptive learning rates.
  
  $$m_t = \beta_1 m_{t-1} + (1 - \beta_1) \frac{\partial L}{\partial w}$$
  
  $$v_t = \beta_2 v_{t-1} + (1 - \beta_2) \left( \frac{\partial L}{\partial w} \right)^2$$
  
  $$\hat{m_t} = \frac{m_t}{1 - \beta_1^t}, \quad \hat{v_t} = \frac{v_t}{1 - \beta_2^t}$$
  
  $$w_{new} = w_{old} - \eta \cdot \frac{\hat{m_t}}{\sqrt{\hat{v_t}} + \epsilon}$$
  
---

# WEEK 2. The Joint Probability
---
The joint probability of multiple random variables can be expressed using the **chain rule of probability**, which breaks down the joint probability into conditional probabilities. The joint probability for $n$ random variables $x_1, x_2, \dots, x_n$ is given by:

$$\large
\textcolor{darkviolet}{
P(x_1, x_2, \dots, x_n) = P(x_1) \cdot P(x_2 | x_1) \cdot P(x_3 | x_1, x_2) \cdots P(x_n | x_1, x_2, \dots, x_{n-1})
}$$

More compactly:

$$\large
\textcolor{darkviolet}{
P(x_1, x_2, \dots, x_n) = P(x_1) \prod_{i=2}^{n} P(x_i | x_1, x_2, \dots, x_{i-1})
}$$

This equation represents how the joint probability of a set of random variables can be decomposed into a product of conditional probabilities.

---

# WEEK 3. The Random Walk with Restart (RWR) Mechanism
---

The **random walk** with a restart mechanism, commonly used when modeling random processes with occasional resets, such as **Google's PageRank** algorithm or other iterative random walk models in network analysis:

$$\large
\textcolor{darkviolet}{
p^{t+1} = (1 - r) M p^t + r \cdot p^0
}$$

Where:
- $p^{t+1}$ is the probability distribution vector at time step $t+1$,
- $p^t$ is the probability distribution vector at time step $t$,
- $p^0$ is the initial probability distribution (i.e., the distribution at $t=0$),
- $M$ is the transition matrix, which represents the probabilities of moving between states in the random walk,
- $r$ is the restart probability (a constant between 0 and 1), which controls how often the walk "restarts" at the initial distribution $p^0$.

### Explanation:
- The term $(1 - r) M p^t$ represents the "normal" random walk step, where $M$ moves the probability mass according to the transition matrix.
- The term $r \cdot p^0$ represents the restart, where with probability $r$, the walker returns to the initial distribution $p^0$.

---

# WEEK 4. Poison Distribution
The Poisson distribution is a discrete probability distribution that expresses the probability of a given number of events occurring in a fixed interval of time or space, given that these events happen with a known constant mean rate and independently of the time since the last event.

The probability mass function of the Poisson distribution is given by:

$$\large
\textcolor{darkviolet}{
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}
}$$

Where:
- \( X \) is the random variable representing the number of events,
- \( k \) is a non-negative integer (the number of events),
- \( \lambda \) is the average rate (or mean) of events per interval,
- \( e \) is the base of the natural logarithm, approximately equal to 2.71828.

### Key Points:
- The parameter \( \lambda \) (lambda) is both the mean and the variance of the distribution.
- The Poisson distribution is suitable for modeling count-based data, such as the number of phone calls received by a call center in an hour or the number of emails received in a day.

### Example Calculation:
If \( \lambda = 3 \) (average rate of 3 events per interval) and you want to find the probability of observing exactly 2 events (\( k = 2 \)):

$$
P(X = 2) = \frac{3^2 e^{-3}}{2!} = \frac{9 e^{-3}}{2} \approx \frac{9 \times 0.0498}{2} \approx 0.224
$$

---

# WEEK 5. Smth

---

# WEEK 6. Network Community Detection - Modularity Q

---

The **modularity Q** measures the strength of the division of a network into communities. It is given by the formula:

$$\large
\textcolor{darkviolet}{
Q = \frac{1}{2m} \sum_{i,j} \left[ A_{ij} - \frac{k_i k_j}{2m} \right] \delta(c_i, c_j)
}$$

Where:
- $A_{ij}$: The adjacency matrix of the network. $A_{ij}$ is 1 if there is an edge between nodes $i$ and $j$, and 0 otherwise.
- $k_i$: The degree of node $i$, i.e., the number of edges connected to node $i$.
- $m$: The total number of edges in the network.
- $c_i$ and $c_j$: The community to which nodes $i$ and $j$ belong, respectively.
- $\delta(c_i, c_j)$: The Kronecker delta function, which is 1 if nodes $i$ and $j$ belong to the same community (i.e., $c_i = c_j$, and 0 otherwise.

### Explanation:

1. **Edge Contribution**: The term $A_{ij} - \frac{k_i k_j}{2m}$ represents the difference between the observed edge weight and the expected edge weight under a random distribution of edges. This accounts for the fact that in a random network, the probability of an edge between nodes $i$ and $j$ is proportional to their degrees $k_i$ and $k_j$.

2. **Community Assignment**: The Kronecker delta function $\delta(c_i, c_j)$ ensures that only pairs of nodes within the same community contribute to the modularity score. If $i$ and $j$ are in the same community, their contribution is included; otherwise, it is excluded.

3. **Normalization**: The modularity is normalized by $\frac{1}{2m}$, which ensures that the modularity score is between -1 and 1.

### Use Case:

Modularity is used to evaluate the quality of a partitioning of a network into communities. Algorithms like the Louvain method or the Girvan-Newman algorithm are often used to find partitions that maximize the modularity.

---

