# KKT Conditions & Power-Grid Attack Detection

**Course:** EECS 127, Optimization Models in Engineering (UC Berkeley, Fall 2024), Homework 8

**Questions:** How do you certify that a candidate answer is optimal, and can an optimization model spot which sensors in a power grid are reporting falsified readings?

## What I did
- **KKT conditions:** proved convexity, verified **Slater's condition**, wrote the **Karush-Kuhn-Tucker (KKT)** conditions and used them to certify a global minimum of a constrained quadratic problem.
- **Maximum likelihood with constraints:** solved a constrained log-likelihood problem of the kind used to estimate **Markov chain transition probabilities**, deriving the optimal solution and optimal value in closed form from the KKT conditions.
- **Resource allocation:** solved an exponential-cost allocation problem with a budget constraint in closed form.
- **Mini-project: attack detection with Lasso (Python, CVXPY):** simulated a 100-node ring power network with random line reactances and phase angles, generated 200 noisy sensor readings (nodal and line power flows), and injected large false-data attacks into 20 of the sensors. I then formulated a **Lasso** model that separates small Gaussian noise (L2 penalty) from sparse attacks (L1 penalty) under the network's power-flow equations, and wrote the success check and a 100-trial harness to estimate how often Lasso finds every attacked sensor.

## What I learned
- KKT conditions turn "is this the best answer?" into a checklist you can verify by hand.
- Lasso's L1 penalty is a practical tool for anomaly detection: it explains most data with small noise and flags the few points that need large corrections.
- Building the simulation (data generation, model, evaluation loop) was as much work as the model itself.

## Skills and tools
KKT conditions, Slater's condition, Lagrangian methods, maximum likelihood estimation, Lasso, sparse anomaly detection, simulation design, Python, CVXPY, NumPy.
