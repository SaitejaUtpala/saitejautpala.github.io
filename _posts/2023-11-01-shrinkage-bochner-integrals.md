---
title: "Shrinkage Estimation of Higher Order Bochner Integrals"
tldr: "Shrinkage estimators of Hilbert-space valued Bochner integrals that strictly improve U-statistics, including a James–Stein result for the normal mean when d ≥ 3. Accepted at Bernoulli, 2023."
tags: [learning theory, statistics]
thumbnail: /assets/updates/bochner-shrinkage/thumb.png
math: true
highlight: true
highlight_title: "Shrinkage Estimation of Higher Order Bochner Integrals"
highlight_venue: "with Bharat K. Sriperumbudur · 2023"
highlight_summary: "We study shrinkage of U-statistic estimators of Hilbert-space valued Bochner integrals toward a target, with oracle inequalities and fast rates. As a special case, in dimension 3 and above the estimator strictly improves the sample mean. Accepted at [Bernoulli](https://projecteuclid.org/journals/bernoulli/volume-30/issue-4/Shrinkage-estimation-of-higher-order-Bochner-integrals/10.3150/23-BEJ1692.short), 2023."
links:
  - name: Paper
    url: https://projecteuclid.org/journals/bernoulli/volume-30/issue-4/Shrinkage-estimation-of-higher-order-Bochner-integrals/10.3150/23-BEJ1692.short
---

**Saiteja Utpala** and Bharat K. Sriperumbudur. Accepted at *[Bernoulli](https://projecteuclid.org/journals/bernoulli/volume-30/issue-4/Shrinkage-estimation-of-higher-order-Bochner-integrals/10.3150/23-BEJ1692.short)*, 2023.

We study shrinkage estimation of higher-order Hilbert space valued Bochner integrals. The idea is
to shrink the $U$-statistic estimator $\hat{C}$ toward a fixed target $f^*$ in the Hilbert space:

$$
\tilde{C} := (1-\hat\alpha)\hat{C} + \hat\alpha f^*.
$$

Depending on the degeneracy of the kernel, these estimators are consistent with fast rates, and we
prove oracle inequalities comparing their risk to that of the unshrunk $U$-statistic. The shrinkage
estimator designed for a completely degenerate kernel remains consistent even when the kernel is
not completely degenerate.

This subsumes and improves earlier results on mean-element and covariance-operator estimation in
RKHSs. Specializing to normal mean estimation, for $d \ge 3$ the estimator **strictly improves**
the sample mean in mean squared error.
