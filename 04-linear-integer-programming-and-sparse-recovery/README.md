# Linear & Integer Programming, Sparse Recovery

**Course:** EECS 127, Optimization Models in Engineering (UC Berkeley, Fall 2024), Homework 7

**Questions:** How do you model a business decision such as a shipping plan as a linear program, and how few measurements do you need to recover a sparse signal?

## What I did
- **LP reformulation:** turned a problem with an exponential objective and norm constraints into an equivalent **linear program**, then rewrote it in LP standard form.
- **Counting LP vertices:** wrote a parallel MATLAB experiment (`parfor`) that enumerates every basic feasible solution of a random 6-constraint, 50-variable LP, and averaged the vertex count over 10 random instances.
- **Integer programming:** formulated the **LP relaxation** of an integer program, solved it in CVX and compared its optimal value with the integer optimum to measure the relaxation gap.
- **Transportation problem:** modeled a two-warehouse, three-customer supply problem with shipping costs and per-unit **penalties for unmet demand**, first as an integer program and then as an equivalent LP, and solved it in CVX for the minimum-cost shipping plan.
- **Compressed sensing:** recovered a 1,000-dimensional signal with only 5 nonzero entries from random linear measurements using **L1-norm minimization**. I ran 10 trials for each measurement count from 5 to 80 and plotted the empirical success probability, which shows a sharp jump from never recovering the signal to almost always recovering it.

## What I learned
- Many real planning problems (shipping, staffing, allocation) are linear programs once the decision variables are chosen well.
- For transportation-type problems the LP relaxation already returns whole-number answers, so the easy problem solves the hard one.
- Sparsity plus L1 minimization lets you recover a signal from far fewer measurements than unknowns, the same idea behind Lasso feature selection.

## Skills and tools
Linear programming, integer programming, LP relaxation, transportation and supply-chain modeling, compressed sensing, L1 minimization, Monte Carlo experiments, parallel computing, MATLAB, CVX.
