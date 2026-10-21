# Multivariate Blink Classification

This directory contains two Jupyter notebooks for multivariate classification of blink responses using DeepLabCut-derived eye-tracking features.

## Analysis Workflow

1. **`blink_reflex_multivariate.ipynb`** — Uses Oracle AutoMLx, originally executed on Oracle's cloud platform, to evaluate candidate machine-learning classifiers and select the best-performing model based on balanced accuracy. The final CatBoost classifier uses six selected feature extrema, as described in the accompanying manuscript.

2. **`blink_reflex_LOMO_validation.ipynb`** — Performs leave-one-group-out cross-validation using the selected six-feature CatBoost classifier with fixed hyperparameters to evaluate generalization across independent groups.

## Input Data

Both notebooks require separately compiled CSV datasets containing trial identifiers, group identifiers, stimulus information, manually scored classification labels, and extracted feature minima and maxima.

Input datasets are not publicly distributed.

## Dependencies

The original classifier selection requires Oracle AutoMLx and its associated environment. The validation notebook uses CatBoost directly, alongside standard Python scientific computing libraries.
