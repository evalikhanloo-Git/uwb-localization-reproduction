# Day 4 – Results Analysis

## Paper
Error Mitigation for TDoA UWB Indoor Localization Using Unsupervised Machine Learning**

## Reading Progress

Completed the Results section and analyzed the experimental evaluation of the proposed method.

---

## Purpose of the Experiments

The authors evaluated whether selecting anchors based on high-quality CIR clusters can improve TDoA indoor localization accuracy.

Instead of using every available measurement, the proposed framework selects only reliable UWB signals for position estimation.

---

## Baseline Methods

The proposed approach was compared with several existing methods:

- Using all available anchors
- Decawave (DW) metrics
- Channel Quality Evaluation (CQE)
- K-Means clustering
- Gaussian Mixture Model (GMM)

These methods represent common approaches for UWB anchor selection and NLoS mitigation.

---

## Evaluation Metric

The main performance metric is:

- Mean Absolute Error (MAE)

Lower MAE indicates higher localization accuracy.

The authors also compare the error distributions of different methods.

---

## Main Findings

The proposed DEC-based framework consistently achieves better positioning accuracy than the baseline methods.

Instead of dividing CIR measurements into only two categories (LoS/NLoS), the proposed method creates multiple clusters with different quality levels.

After ranking these clusters, only measurements from high-quality clusters are used for localization.

This strategy removes unreliable measurements while preserving more useful information for position estimation.

---

## Why Does the Proposed Method Perform Better?

From my understanding, the main reason is that the proposed framework does not simply classify signals as LoS or NLoS.

Instead, it evaluates the quality of different CIR clusters and keeps only the most reliable measurements.

This produces cleaner input data for the localization algorithm and reduces the influence of NLoS and multipath propagation.

---

## What I Learned Today

Today I realized that improving localization accuracy is not always achieved by designing a new localization algorithm.

Sometimes, improving the quality of the input data before localization can significantly improve the final positioning accuracy.

This paper demonstrates that intelligent data selection can be as important as the localization algorithm itself.

---

## Personal Reflection

Today I learned that improving localization accuracy is not simply achieved by removing NLoS measurements.

If too many measurements are discarded, the localization algorithm may not have enough information for accurate position estimation.

The proposed DEC framework addresses this problem by identifying multiple quality levels instead of using only two classes (LoS/NLoS).

This allows the system to preserve sufficient useful measurements while filtering out unreliable ones, leading to a better balance between data quality and data availability.
