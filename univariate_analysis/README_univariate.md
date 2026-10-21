# Univariate Blink Classification

This directory contains two Jupyter notebooks for feature extraction and threshold-based blink classification using DeepLabCut-derived eyelid keypoint coordinates.

## Analysis Workflow

1. **`[1]Blink_feature_min_max_calculations.ipynb`** — Calculates six blink features (Euclidean distance, eye aspect ratio, inner eye angle, outer eye angle, eye velocity, and eye area) from DeepLabCut-generated CSV files and extracts feature minima and maxima.

2. **Intermediate data preparation** — The extracted minimum and maximum values are manually compiled in Microsoft Excel into the required CSV structure for subsequent analysis.

3. **`[2]Blink_feature_thresholds_versus_accuracy_plots.ipynb`** — Determines Otsu thresholds and compares classification accuracy against manually selected thresholds using manually scored reference labels. Generates threshold and accuracy plots.

## Input Data

The notebooks require DeepLabCut-generated keypoint CSV files and manually compiled feature tables. Input directories are configured using `folder_path`.

Input datasets are not publicly distributed.

## Dependencies

Python, Jupyter Notebook, and associated scientific computing libraries. The notebooks were originally developed for use in Google Colab with Google Drive-mounted data.
