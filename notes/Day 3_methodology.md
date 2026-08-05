# 3 – Methodology Analysis

## Error Mitigation for TDOA UWB Indoor Localization Using Unsupervised Machine Learning**

## Reading Progress

Completed the first part of the Methodology section.

## Main Input

The proposed framework uses **raw Channel Impulse Response (CIR)** data collected from the UWB receiver as the input.

## Role of the DEC Algorithm

The proposed method is based on the **Deep Embedded Clustering (DEC)** algorithm.

The DEC framework consists of two main components:

- An **Autoencoder** that learns a compact latent representation of the input CIR data.
- A **Clustering Layer** that groups similar CIR measurements into multiple clusters.

Unlike conventional clustering methods, DEC simultaneously learns feature representations and cluster assignments.

## Methodology Workflow

1. Collect raw CIR measurements.
2. Apply the DEC algorithm to learn feature representations and cluster the CIR data.
3. Evaluate the quality of each cluster.
4. Rank the clusters based on their quality.
5. Select high-quality clusters for localization.
6. Estimate the tag position using the selected measurements.

## Cluster Quality Evaluation

The quality of each cluster is evaluated using the distance between the **First Path Index (FP)** and the **Peak Path Index (PP)**.

For each cluster, the authors calculate:

- Mean distance
- Standard deviation

These statistical metrics are used to rank the clusters and identify high-quality clusters for position estimation.

## Key Takeaways

- The framework uses raw CIR data as its input.
- DEC learns meaningful feature representations while clustering the CIR measurements.
- Cluster quality evaluation is performed before localization.
- Selecting high-quality clusters improves TDoA localization accuracy.

## Personal Reflection

Today I understood the overall methodology of the proposed framework. I learned how the DEC algorithm, cluster quality evaluation, and cluster selection work together to improve indoor UWB TDoA localization accuracy. Compared with the Introduction, I now have a much clearer understanding of how the complete framework operates.
