# Image Enhancement and Segmentation using Brain Tumor Datatset

This project demonstrates a **comprehensive image-processing pipeline** for medical MRI images, integrating three classical techniques for image enhancement, segmentation, and feature extraction. The pipeline is implemented in Python using OpenCV, NumPy, and Matplotlib.

---

## Overview

Medical imaging often requires preprocessing to improve visibility, highlight regions of interest, and extract structural features. This pipeline applies the following techniques to MRI scans:

1. **CLAHE (Contrast Limited Adaptive Histogram Equalization):** Enhances image contrast adaptively for better visibility of subtle structures.
2. **GrabCut Segmentation:** Semi-automatically segments the main region of interest using a bounding rectangle initialization.
3. **Canny Edge Detection:** Identifies edges and structural boundaries for feature analysis.

The pipeline also includes automatic visualization of the original and processed images for immediate evaluation.

---
## Installation & Setup

1. Clone the Repository
`bash`
```
git clone <your-repo-url>
cd <repo-folder>
```

2. Create a Virtual Environment 
```
python -m venv venv

Activate

Windows:
venv\Scripts\activate

macOS/Linux:
source venv/bin/activate
```

3. Install Dependencies
```
pip install opencv-python numpy matplotlib
```
---

## Techniques

### 1. CLAHE (Contrast Limited Adaptive Histogram Equalization)

* Enhances local contrast in the image.
* Particularly effective for low-contrast MRI scans.
* Implemented by converting the image to LAB color space and applying CLAHE on the L-channel.

### 2. GrabCut Segmentation

* Semi-automatic segmentation algorithm to isolate regions of interest.
* Uses a rectangular initialization and iterative refinement of foreground and background.
* Outputs both the segmented image and a binary mask.

### 3. Canny Edge Detection

* Detects edges by analyzing intensity gradients.
* Preprocessing includes grayscale conversion and Gaussian blurring to reduce noise.
* Highlights structural boundaries within the image.

---

## Visualization

Each technique generates a clear visualization including:

* **Original Image**
* **Processed Output** (Enhanced / Segmented / Edges)

Visualizations are implemented using `matplotlib` for high-quality, publication-ready figures.

---

## Features

* Object-oriented design for modularity and reusability.
* Logging enabled for step-by-step execution tracking.
* Error handling for robust processing of different input images.


---

## References

* OpenCV Documentation: [https://opencv.org/](https://opencv.org/)
* Gonzalez, R. C., & Woods, R. E. *Digital Image Processing*. Pearson.
* [Dataset Used](https://universe.roboflow.com/roboflow-100/brain-tumor-m2pbp)
