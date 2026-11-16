# Duality, Matrix Completion & Newton's Method

**Course:** EECS 127, Optimization Models in Engineering (UC Berkeley, Fall 2024), Homework 9

**Questions:** How do you fill in a ratings matrix from a small sample of its entries, and how do you write your own solver that converges reliably?

## What I did
- **Lagrange duality:** derived the dual of a quadratically constrained quadratic program (QCQP) and used **weak duality** to produce a certificate that a set of equations has no solution.
- **Optimality conditions for resource allocation:** derived necessary and sufficient conditions for splitting a limited budget across tasks with concave rewards.
- **Netflix-style matrix completion (Python, CVXPY):** generated random rank-one 200 × 200 matrices, revealed only 10% of their entries, and recovered the full matrix with **nuclear-norm minimization**. Over 20 random trials, every recovery met the accuracy threshold.
- **Newton's method from scratch (NumPy):** implemented Newton's method with an analytic gradient and Hessian for a 1,000-variable convex problem.
  - With a **constant step size**, iterations to converge fell from 177 at a step of 0.25 to 39 at 1.25, then rose to 57 at 1.5 and 66 at 1.75 as steps overshot.
  - I then added **backtracking line search**, which adapts the step each iteration, and plotted the distance to the optimum on a log scale.

## What I learned
- Low-rank structure is what makes recommender-system style completion possible from a small sample, and the nuclear norm is the convex way to ask for it.
- Step-size choice decides how fast a second-order method converges; backtracking picks the step automatically, though its own parameters still matter.
- Duality gives cheap certificates: a single feasible dual point can prove that no solution exists.

## Skills and tools
Lagrange duality, QCQP, KKT conditions, matrix completion, nuclear-norm minimization, recommender systems, Newton's method, backtracking line search, Python, CVXPY, NumPy, Matplotlib.
