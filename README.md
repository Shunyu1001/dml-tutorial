# AIPW and Double Machine Learning: From Theory to Code

**Shunyu Hao**, PLSC 40601, University of Chicago, Spring 2026

## About

This is a tutorial on the Augmented Inverse Probability Weighting (AIPW) estimator and the Double Machine Learning (DML) framework. It covers the theory and the code.

## Contents

The tutorial has 7 sections:

1. Background: the potential outcomes framework and the ATE
2. Three estimation strategies: OR, IPW, and AIPW
3. The efficient influence function and semiparametric efficiency
4. Neyman orthogonality
5. Double Machine Learning: cross-fitting and the product rate condition (detailed code)
6. Monte Carlo simulation: how nuisance learner choice affects DML
7. Discussion and takeaways

## Key Results

The notebook includes three visualizations and a Monte Carlo simulation that compares four ML learners (Lasso, Random Forest, Gradient Boosting, Neural Network) under two DGPs.

**Sparse DGP (p = 50, linear):**

| Learner | Bias | RMSE | 95% CI Coverage |
|---|---|---|---|
| Lasso | -0.059 | 0.128 | 90% |
| Random Forest | +0.349 | 0.385 | 20% |
| Gradient Boosting | +0.042 | 0.191 | 90% |
| Neural Network | +5.302 | 5.388 | 0% |

**Smooth DGP (p = 10, nonlinear):**

| Learner | Bias | RMSE | 95% CI Coverage |
|---|---|---|---|
| Lasso | -0.035 | 0.143 | 100% |
| Random Forest | -0.035 | 0.165 | 90% |
| Gradient Boosting | +0.017 | 0.231 | 90% |
| Neural Network | -0.388 | 0.442 | 50% |

The main takeaway: learner choice matters a lot. When the learner does not fit the DGP well, the product rate condition fails, and DML gives large bias and poor coverage.

## How to Run

Open `tutorial.ipynb` in Jupyter Notebook or JupyterLab. The notebook already contains all outputs, so you can read it without running any code.

To rerun from scratch:

```
pip install numpy pandas scikit-learn matplotlib lightgbm
```

The notebook runs from top to bottom. Section 6 (Monte Carlo simulation with 10 repetitions) takes about 1 minute.

## References

- Chernozhukov, V. et al. (2018). Double/debiased machine learning for treatment and structural parameters. The Econometrics Journal, 21(1), C1-C68.
- Hahn, J. (1998). On the role of the propensity score in efficient semiparametric estimation of average treatment effects. Econometrica, 66(2), 315-331.
- Kennedy, E. H. (2022). Semiparametric doubly robust targeted double machine learning: A review. arXiv:2203.06469.
