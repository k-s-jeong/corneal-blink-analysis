# Corneal Blink Analysis

This repository contains Python-based analysis code for automated detection and classification of blink responses using six features derived from DeepLabCut-tracked eyelid keypoints: Euclidean distance, eye aspect ratio (EAR), inner eye angle, outer eye angle, eye velocity (change in Euclidean distance), and eye area.

## Analysis Workflows

- **Univariate analysis:** Extracts blink features from DeepLabCut-generated CSV files, calculates feature minima and maxima, and evaluates classification accuracy using Otsu-derived and manually selected thresholds against manually scored reference labels. Intermediate data compilation is performed manually in Excel.

- **Multivariate analysis:** Uses separately compiled trial-level feature datasets for machine-learning classifier selection through Oracle AutoMLx, followed by leave-one-group-out validation using CatBoost.

## Data Availability

The repository provides analysis notebooks and documentation. Original input datasets, video recordings, and supporting tracking resources are not publicly distributed.

The workflows and methodological details are described in the accompanying *Journal of Neuroscience Methods* manuscript.