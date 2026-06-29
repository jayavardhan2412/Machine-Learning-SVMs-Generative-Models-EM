# CS771: Introduction to Machine Learning — Project Portfolio

This repository contains three end-to-end algorithmic implementations developed for the **CS771: Introduction to Machine Learning** course under Professor Mainak Chaudhuri at the Indian Institute of Technology (IIT) Kanpur (2025–26). The portfolio covers supervised linear margin classification, probabilistic generative modeling under incomplete information, and unsupervised latent-variable mixture regression.

## Core Assignments & Methodologies

### 1. SVM Boundary Mechanics & Constraint Limits (`Assignment-1`)
An empirical investigation into the geometric properties and optimization limits of linear margin classifiers.

* **Geometric Separability Proof:** Demonstrated via geometric margin analysis that synthetically generated multi-cluster data is strictly linearly separable, confirming the altitude of the separation boundary strictly exceeds the class radii ($h > 2$).
* **Systematic Evaluation:** Analyzed `LinearSVC` stability across extreme low, medium, and high difficulty regimes by shifting the regularization penalty, stopping tolerances, and maximum iterations.
* **Extreme Constraint Mapping:** Established the exact minimal regularization bounds and iteration thresholds required to achieve absolute convergence without solver warnings across varying margin widths.
* **Key Topics:** Linear SVMs, Regularization Dynamics, Mathematical Optimization, Margin Boundaries, Bias-Variance Tradeoff.

### 2. Generative Gaussian Image Reconstruction (`Assignment-2`)
A probabilistic modeling framework developed to classify digits and reconstruct missing pixels under aggressive censoring using per-class Gaussian generative models.

* **Single-Step Joint MAP Inference:** Formulated a Maximum A Posteriori (MAP) estimator that unifies classification objectives and pixel imputation into a single joint optimization step, penalized by a log-determinant uncertainty term.
* **Algorithmic Efficiency:** Restructured the computational pipeline to precompute inverse covariance matrices and evaluate reconstruction math exclusively for the winning class, effectively bypassing continuous matrix recalculations.
* **Inference Scaling Discovery:** Quantified the inverse relationship between inference latency and missing pixel proportion, driven by the $O(d_o^3)$ pseudo-inverse dimensionality on the observed pixel matrix.
* **Key Topics:** Gaussian Generative Models, MAP Inference, Image Censoring, Numerical Matrix Stability, Joint Optimization.

### 3. EM Mixture Regression for Air Quality Forecasting (`Assignment-3`)
An unsupervised mixture modeling approach implemented to forecast ground-level ozone concentrations from IoT environmental sensor datasets.

* **Convergence and Stability:** Mapped the Expectation-Maximization (EM) algorithm's optimization trajectory to identify the absolute convergence knee point, bypassing early transient minimums caused by hard-assignment initializations.
* **Complexity Selection & Ablation:** Identified an optimal model complexity of K = 4 components to partition the feature space into interpretable pollution regimes; isolated ambient temperature as the most critical physical proxy for ozone prediction.
* **Structural Benchmarking:** Benchmarked the EM mixture model against deep `DecisionTreeRegressor` architectures, highlighting a fundamental trade-off between the high-speed scalar inference of decision trees and the superior accuracy of localized linear regression experts.
* **Key Topics:** Expectation-Maximization Algorithm, Mixture Models, Ridge Regression, Feature Ablation, Decision Trees.

---

## Academic Documentation

Each project directory (`Assignment-1`, `Assignment-2`, `Assignment-3`) contains the complete Python implementation accompanied by a formal **NeurIPS-style LaTeX conference report** detailing mathematical derivations, experimental setups, and error analyses.

---

## Authors

**Group:** Optimizers  
**Course:** CS771: Introduction to Machine Learning  
**Institution:** Indian Institute of Technology (IIT) Kanpur (2025–26)
