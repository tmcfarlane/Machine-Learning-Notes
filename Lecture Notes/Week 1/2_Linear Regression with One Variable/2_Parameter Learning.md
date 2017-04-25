# Gradient Descent

**Outline:**
1. Start with some Θ<sub>0</sub>, Θ<sub>1</sub> Ex. (0, 0)
2. Keep changing Θ<sub>0</sub>, Θ<sub>1</sub> to reduce J(Θ<sub>0</sub>, Θ<sub>1</sub>) until we hopefully end up at a minimum

Side Note: Gradient Descent ends up solving a more general problem such as if you had 0...n number of parameters.

**Definition:**
Looking 360 degrees around your point, take a step towards the fastest descent possible. Continue until you've created the furthest descent possible on your path.

By changing your starting point by a little bit my change your ending point drastically.

### Gradient Descent Algorithm
![Gradient Descent Algorithm](img/gradient_descent_algorithm.png)

**Breakdown:**

`:=` = assignment operator
`α` = learning rate (corresponds to size of steps being made)

For this equation (the algorithm) we want to simultaneously update Θ<sub>0</sub> and Θ<sub>1</sub>.

If you do not update simultaneously the algorithm is not implemented correctly, as the values Θ<sub>0</sub> and Θ<sub>1</sub> are dependent on each other when updating.