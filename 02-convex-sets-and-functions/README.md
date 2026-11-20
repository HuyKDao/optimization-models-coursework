# Convex Sets & Functions

**Course:** EECS 127, Optimization Models in Engineering (UC Berkeley, Fall 2024), Homework 5

**Question:** How do you prove a problem is convex, and so safe to hand to a solver, without guessing?

## What I did
- **Convexity proofs from first principles:** proved convexity using the definition (zeroth-order condition), restriction to a line, and composition rules (convex, non-decreasing outer functions), including for sums of exponentials and reciprocal-type functions.
- **Hessian checks:** used Hessian eigenvalues to show how a large enough quadratic penalty turns a non-convex function into a convex one.
- **Convex sets:** showed that sublevel sets of convex functions and intersections of convex sets stay convex, and applied this to a set defined by several nonlinear inequalities.
- **Separating hyperplanes in CVX:** proved a distance-based test for whether two sets overlap. Then I wrote a MATLAB/CVX program that computes the closest pair of points between two convex sets and builds the hyperplane that separates them.

## What I learned
- A short list of composition rules covers most functions that show up in data science objectives (log-sum-exp, norms, penalties).
- Distance between sets is itself an optimization problem, and its solution gives a certificate (a separating hyperplane), which is the same idea behind support vector machines.

## Skills and tools
Convex analysis, proof writing, Hessian and eigenvalue analysis, separating hyperplane theorem, MATLAB, CVX.
