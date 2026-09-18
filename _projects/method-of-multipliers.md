---
title: "General-Kernel Augmented Lagrangian Methods for GPU-Accelerated Nonlinear Programming"
collection: projects
excerpt: "A general-kernel augmented-Lagrangian framework for large-scale, degenerate nonlinear programs on GPUs."
order: 1
---

**Status:** Ongoing (since May 2026) &middot; **Advisor:** [Sungho Shin](https://cheme.mit.edu/profile/sungho-shin/) &middot; **Affiliation:** Massachusetts Institute of Technology (research internship)

Interior-point and SQP solvers are hard to map efficiently onto GPUs, because each iteration factorizes a sparse, possibly indefinite KKT matrix whose numerical pivoting is inherently sequential. Augmented Lagrangian methods are an attractive alternative on two counts: they degrade gracefully on *degenerate* problems, whose feasible points violate constraint qualifications such as LICQ or MFCQ, since the penalty acts as a dual regularization; and they fail *informatively* on infeasible instances, where the iterates converge to a minimizer of an infeasibility merit.

This project generalizes Algorithm NCL — an augmented Lagrangian method for large-scale, degenerate nonlinear programs — by replacing its uniform quadratic penalty with per-constraint weight–kernel pairs (γ, φ). The penalty kernel determines both the multiplier update and the curvature the penalty contributes to the subproblem KKT systems, yet it has remained fixed and quadratic in existing augmented Lagrangian implementations. The framework turns the kernel, together with the weights, into algorithm design degrees of freedom.

On the theory side, local exactness at finite penalty holds uniformly over the framework under mild assumptions, and every member preserves the symmetric quasi-definite KKT structure that admits sparse LDL<sup>T</sup> factorization with static pivoting — the property that makes the whole family GPU-friendly. Every generated sequence of iterates follows one of two branches: either the acceptance test succeeds infinitely often and the accepted iterates approach feasible points, which are KKT points whenever the multiplier estimates remain bounded, or the iterates approach a stationary point of an infeasibility merit selected by the weights and kernels.

Building on the framework, we design a GPU implementation that exercises the weight degree of freedom through adaptive weights driven by constraint geometry, together with an acceptance test calibrated in residual units for every admissible kernel. Numerical experiments on constrained CUTEst instances, PGLIB optimal power flow, COPS benchmarks, and security-constrained optimal power flow with complementarity constraints show improved robustness over NLP solver baselines at comparable factorization cost, while effectively managing problem degeneracy — including equality-over-determined systems and MPCC constraints.

This is active work; code and writeups are not yet public.
