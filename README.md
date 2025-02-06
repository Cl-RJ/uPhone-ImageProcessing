# µ-phone: Image Processing and Analysis for Accessible Microscope Attachment

This repository contains the code and workflows for processing and analyzing images captured using the µ-phone, an accessible microscope attachment for smartphones. The µ-phone enables point-of-care (POC) diagnostics at a cellular level using low-cost components, making it ideal for resource-limited settings.

## Project Overview

The image processing code enhances microscopic images captured with the µ-phone. It focuses on improving clarity, reducing noise, and analyzing intensity profiles along specified lines for metrics evaluation. The project demonstrates the capability of the µ-phone system to observe human blood smears and optical targets.

## Features

- **Preprocessing**:
  - Circular masking to isolate regions of interest.
  - Intensity normalization to mitigate lighting variations.

- **Image Enhancement**:
  - Noise reduction using Gaussian and median filters.
  - Edge enhancement through sharpening and contrast adjustments.
  - Histogram equalization using CLAHE for improved visibility.

- **Analysis**:
  - Clarity metrics: Variance of Laplacian, Tenengrad, and Shannon entropy.
  - Intensity profile extraction along specified lines.
  - Visualization of original, enhanced, and reference images side by side.

## Installation

1. Clone this repository:
    ```bash
    git clone https://github.com/Cl-RJ/uPhone-ImageProcessing.git
    cd microphone-image-processing
    ```

2. Set up the Python environment:
    ```bash
    conda create -n microphone python=3.8
    conda activate microphone
    pip install -r requirements.txt
    ```

3. Required Python packages include:
   - `opencv-python`
   - `numpy`
   - `matplotlib`
   - `scipy`
   - `skimage`

## Usage

1. Place your images (e.g., blood smears or USAF optical targets) in the working directory.
2. Open the Jupyter Notebook (`Image_Processing_Final.ipynb`).
3. Update the `image_prefix` variable to match your input file (e.g., `'RBC'`, `'USAF'`, or `'grid'`).
4. Run the notebook to process images, calculate clarity metrics, and visualize results.

## Workflow

1. **Image Preprocessing**:
   - Define circular masks to focus on regions of interest.
   - Normalize intensity for consistent illumination.

2. **Image Enhancement**:
   - Sequential application of Gaussian blur, sharpening, and median filtering.
   - Contrast enhancement with adaptive histogram equalization.

3. **Analysis and Visualization**:
   - Extract intensity profiles along predefined lines.
   - Calculate clarity metrics for comparison between original and enhanced images.
   - Display images and corresponding intensity profiles side by side.

## Example Results

- **Clarity Metrics**:
  - Variance of Laplacian (sharpness).
  - Tenengrad (gradient magnitude).
  - Shannon Entropy (randomness/complexity).

- **Visualization**:
  - Original, enhanced, and reference images with intensity profiles plotted for comparative analysis.

## Citation

If you use this code or the µ-phone system in your research, please cite:

```
@article{song2025microphone,
  title={µ-phone: Accessible Microscope Attachment for Smartphones},
  author={Song, Kefan and Wu, Sixuan and Peng, Ruijia and Cobb, Jason and Adams, Alexander},
  journal={Point-of-Care Technologies},
  year={2025}
}
```

## Acknowledgments

The µ-phone system was developed by researchers at the Georgia Institute of Technology and Emory University. This project leverages their expertise in biomedical engineering and interactive computing to create affordable diagnostic tools.