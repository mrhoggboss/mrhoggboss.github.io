---
title: "Kernel-Agnostic Method of Multipliers for GPU-Accelerated Nonlinear Programming"
collection: projects
excerpt: "A GPU-friendly augmented-Lagrangian framework for large-scale constrained nonlinear programs."
order: 1
---

**Status:** Ongoing (since May 2026) &middot; **Advisor:** [Sungho Shin](https://cheme.mit.edu/profile/sungho-shin/) &middot; **Affiliation:** Massachusetts Institute of Technology (research internship)

Modern interior-point and SQP solvers for nonlinear programming are hard to map efficiently onto GPUs, because the linear systems they solve change sparsity and conditioning from iteration to iteration. This project investigates GPU-friendly augmented-Lagrangian / method-of-multipliers algorithms for large-scale constrained NLPs, focusing on how the choice of *penalty kernel* shapes the conditioning and GPU-factorizability of the resulting KKT system.

A central thread is a mixed-kernel formulation that pairs a quadratic equality kernel (in the spirit of NCL) with an exponential inequality kernel, collapsing inequality handling into a single equality-constrained Newton solve while preserving a regular, GPU-friendly KKT structure.

This is active work; code and writeups are not yet public.
