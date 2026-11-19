# Convex Optimization & LP Geometry

**Course:** EECS 127, Optimization Models in Engineering (UC Berkeley, Fall 2024), Homework 6

**Question:** When does an optimization problem have a solution at all, when is every local solution the best one, and where do linear programs land their answers?

## What I did
- **Is it a convex problem?** Found the coefficients that make a constrained polynomial problem a convex optimization problem.
- **Existence and global optimality:** checked feasibility, used the **Weierstrass theorem** to prove a solution exists on a closed, bounded feasible set, and proved every local minimum is global by showing the problem is convex.
- **Reasoning about convex functions:** proved from a few known values of a convex function which other points are, or can't be, its minima.
- **Coercivity:** proved when functions grow without bound in every direction (coercive), which guarantees a minimum exists.
- **LP vertices by simulation:** ran a 100-trial Monte Carlo experiment in MATLAB/CVX, solving a small linear program with a random cost vector each time, and used the frequency of each optimal solution to empirically find the vertices of the feasible region and the probability that each one is optimal. The four vertices were optimal in 32%, 31%, 21% and 16% of trials.

## What I learned
- Theory tells you whether a solver's answer can be trusted before you run it.
- A linear program over a bounded region always has an optimal corner, and simulation is a quick way to see which corners matter most.

## Skills and tools
Convex optimization, Weierstrass theorem, coercive functions, linear programming geometry, Monte Carlo simulation, MATLAB, CVX.
