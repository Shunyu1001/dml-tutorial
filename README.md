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

## How to Run

Open `tutorial.ipynb` in Jupyter Notebook or JupyterLab.

Requirements:

```
pip install numpy pandas scikit-learn matplotlib lightgbm
```

The notebook runs from top to bottom. Section 6 (Monte Carlo simulation) takes a few minutes.

## References

- Chernozhukov, V. et al. (2018). Double/debiased machine learning for treatment and structural parameters. The Econometrics Journal, 21(1), C1-C68.
- Hahn, J. (1998). On the role of the propensity score in efficient semiparametric estimation of average treatment effects. Econometrica, 66(2), 315-331.
- Kennedy, E. H. (2022). Semiparametric doubly robust targeted double machine learning: A review. arXiv:2203.06469.
