# Linear Systems & Robust Regression

**Course:** EECS 127, Optimization Models in Engineering (UC Berkeley, Fall 2024), Homework 3

**Questions:** Which targets can a simple linear system actually reach, and what is the cheapest way to get there? And when a few measurements are corrupted, should you fit with least squares or least absolute deviations?

## What I did
- **Reachability with linear algebra:** modeled a small drone-style system whose position updates linearly with each control input, built its control matrix, and used the null space and range of that matrix to show exactly which target positions can and can't be reached.
- **Minimum-energy control in CVX:** formulated the "reach the target using the least total input energy" problem as a convex program, solved it in MATLAB/CVX and plotted the 3D trajectory. Then I added box-shaped **safety constraints** on every position and compared the new optimal path with the unconstrained one.
- **L1 vs. L2 regression under outliers:** ran a grid experiment over 6,561 outlier patterns (an 81 × 81 grid of sizes for two corrupted measurements), solving both a least-absolute-deviations (L1) and a least-squares (L2) fit for each, and mapped which estimator recovered the true parameters better. The map split into clean symmetric regions depending on the signs of the two outliers, which made the robustness trade-off between the two losses visible.
- **Optimality from calculus:** used the gradient and Hessian of a two-variable objective to prove that a candidate point is its global minimum.

## What I learned
- Range and null space answer practical "is this even possible?" questions before any optimization is run.
- Adding constraints to a convex problem is cheap to model, and re-solving shows exactly how safety limits change the plan.
- The choice of loss function matters: L1 is more forgiving of some outlier patterns, L2 of others.

## Skills and tools
MATLAB, CVX, linear algebra (range, null space, rank), least squares, least absolute deviations (L1 regression), constrained optimization, 3D plotting.
