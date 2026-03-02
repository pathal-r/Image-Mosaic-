# Image Mosaic

Image mosaicing pipeline that stitches multiple overlapping images into a single panoramic view using homography estimation and pose graph optimization.

## Overview

This project implements two approaches to image mosaicing from a set of six input images. The first approach iteratively computes pairwise homographies to warp and blend images into a panoramic mosaic. The second constructs and optimizes a pose graph over the image set. The full pipeline is provided in the Jupyter notebook.

## Pipeline

```
6 Input Images ──► Pairwise Feature Matching ──► Homography Estimation ──► Image Warping ──► Panoramic Mosaic
                                                                       └──► Pose Graph Generation ──► Graph Optimization
```

## Methodology

### Part 1(a) — Panoramic Stitching
- Iterates through six images, computing homography between consecutive pairs
- Warps each image into a common reference frame using the estimated homographies
- Combines warped images into a single panoramic mosaic

### Part 1(b) — Pose Graph Optimization
- Generates a pose graph from the six-image dataset using pairwise geometric relationships
- Optimizes the pose graph to refine relative camera poses
- Visualizes the graph structure and optimization results via `matplotlib`

## Tech Stack

`Python` · `OpenCV` · `NumPy` · `Matplotlib` · `Jupyter`

## Getting Started

```bash
git clone https://github.com/pathal-r/Image-Mosaic-.git
cd Image-Mosaic-
pip install numpy opencv-python matplotlib
jupyter notebook "Image Mosaic.ipynb"
```

The notebook contains the complete implementation with visualizations of the stitched panorama and pose graph.
