---
title: "Wasserstein Motifs: Optimal Transport for Ecological Network Alignment"
collection: projects
excerpt: "A rigorous, scalable optimal-transport framework for aligning food webs and extracting interaction backbones."
order: 4
---

**Status:** Ongoing (since May 2024) &middot; **Advisors:** [César A. Uribe](https://cauribe.rice.edu/), Lydia Beaudrot &middot; **Affiliations:** Rice University & Michigan State University

We study ecological network (food web) alignment: identifying structural equivalences among species and uncovering *backbones of interactions* that represent shared functional substructures. Existing approaches are computationally expensive, hard to scale, and difficult to interpret ecologically.

We give a first rigorous formalization of food web alignment based on network motifs, and show that methods popularized in the ecological community are equivalent to minimizing a Fused Gromov–Wasserstein-like cost functional — what we term *Wasserstein Motifs*. We propose an interpretable, provably correct algorithm that efficiently computes non-deterministic alignments by treating food webs as feature measure networks, and as a byproduct, a new way to identify non-deterministic interaction backbones. On a continental-scale dataset of 129 Sub-Saharan African mammal food webs, the method delivers large gains in accuracy, a 158× speedup, and improved interpretability over the state of the art. An extended journal manuscript is in preparation.

**Materials**

- Conference paper — *Identifying Common Backbones of Interactions Underlying Food Webs via Non-Deterministic Alignments*, ICASSP 2026: [IEEE Xplore](https://ieeexplore.ieee.org/document/11462837) ([DOI](https://doi.org/10.1109/ICASSP55912.2026.11462837)) &middot; [author copy with appendix (PDF)](/files/WassMotif_ICASSP_with_app.pdf)
- Extended manuscript — *Wasserstein Motifs: Non-deterministic Alignment of Ecological Networks*, LMRL Workshop @ ICLR 2026 (oral, non-archival): [OpenReview](https://openreview.net/forum?id=ys92oWSFiB)
- [Slides](https://drive.google.com/file/d/1Rm1sPLYEd6ZFSrDLmz8hKLddOFoUy5cL/view) — INFORMS Optimization Society Conference 2026 (oral presentation)
- [Poster (PDF)](/files/Wasserstein_Motifs_TL;DR_Conference_Poster.pdf) — ICASSP 2026 / Texas Colloquium on Distributed Learning ([related page](/publication/wasserstein-motifs))
- [Course report (PDF)](/files/COMP_414_Final_Report.pdf)
