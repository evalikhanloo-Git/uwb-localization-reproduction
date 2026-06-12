# Day 2 – Introduction Analysis

# Error Mitigation for TDOA UWB Indoor Localization Using Unsupervised Machine Learning

## Reading Progress
 Completed the Introduction section.


## Main Problem

The paper addresses positioning errors in UWB TDoA indoor localization systems caused by:

- Non-Line-of-Sight (NLoS) conditions
- Multipath propagation

These effects introduce biases in ranging measurements and reduce localization accuracy.


## Why is this important?

Accurate indoor positioning is required for:

- Industrial IoT applications
- Automated Guided Vehicles (AGVs)
- Forklift tracking
- Indoor asset localization


## Previous Approaches

The paper discusses:

1. Statistical methods based on CIR analysis.
2. Machine learning approaches:
   - Supervised learning
   - Unsupervised learning

Supervised methods provide good performance but require extensive data labeling.

Unsupervised approaches such as K-Means and GMM avoid labeling requirements but have 
limitations when applied to large datasets and complex environments.



## Key Observation

Using only two clusters (LoS / NLoS) may be insufficient in dense multipath 
environments because too few reliable measurements remain available for localization.


## Authors' Contribution
The authors propose:

- A Deep Embedded Clustering (DEC) framework
- Cluster quality evaluation
- Selection of high-quality clusters for position estimation

The goal is to reduce localization error without requiring labeled training data.


## Personal Notes

The most interesting idea in the introduction is that the authors do not simply 
classify measurements as LoS or NLoS. Instead, they create multiple clusters, evaluate 
their quality, and use only the most reliable measurements for localization.
