---
title: "GPU-Accelerated Bregman Douglas–Rachford Splitting for Discrete Optimal Transport"
collection: projects
excerpt: "A scalable first-order solver for large-scale discrete optimal transport on the GPU."
order: 2
---

**Status:** Ongoing (since October 2025) &middot; **Advisor:** [Shiqian Ma](https://sqma.rice.edu/) &middot; **Affiliations:** Rice University & Johns Hopkins University

This project develops a GPU-accelerated solver for large-scale Discrete Optimal Transport (the Kantorovich problem) based on Bregman Douglas–Rachford splitting, using entropy/Bregman geometry to keep iterates numerically stable.

By deriving a factored log-domain representation of the transport plan and exploiting separability of grid-based cost functions, the method cuts the per-iteration cost from quadratic, O(N²), to roughly O(N¹·⁵), and reduces memory from about 550 GB to 20 MB at a 512×512 resolution. A *c*-transform dual post-processing step produces by-construction feasible dual certificates, reducing the iterations needed to reach a 10⁻⁴ KKT residual by about 82% on the DOTmark benchmark and settling every instance faster than state-of-the-art GPU OT solvers. The solver is implemented with fused CUDA kernels and CUDA Graphs.

A manuscript is in preparation; materials are not yet public.
