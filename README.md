# Image Mosaic

An image mosaicing (stitching) pipeline that combines multiple overlapping images into a single panoramic view using feature matching and homography estimation.

## Overview

This project implements an image mosaicing algorithm that detects keypoints across overlapping images, matches corresponding features, estimates homography transformations, and warps images into a unified panoramic mosaic. The full pipeline and detailed explanation are provided in the Jupyter notebook.

## Pipeline

```
Input Images ──► Feature Detection ──► Feature Matching ──► Homography Estimation ──► Image Warping ──► Panoramic Mosaic
```

## Tech Stack

`Python` · `OpenCV` · `NumPy` · `Jupyter`

## Getting Started

```bash
git clone https://github.com/pathal-r/Image-Mosaic-.git
cd Image-Mosaic-
jupyter notebook "Image Mosaic.ipynb"
```

The notebook contains the complete implementation with step-by-step explanations and visualizations.
