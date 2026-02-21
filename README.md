[![DOI](https://zenodo.org/badge/1163455168.svg)](https://doi.org/10.5281/zenodo.18725821)
# Brand-Detection-Dataset-Notebook

## Overview

This repository provides the training and evaluation notebook for the **Product Brand Detection dataset**, a multi-class object detection dataset designed for recognizing consumer product brands in retail environments.

The notebook demonstrates end-to-end experimentation including dataset loading, model training, evaluation using COCO metrics, per-class performance analysis, and inference visualization.

The dataset associated with this repository is publicly available on IEEE DataPort.

---

## Dataset

**Dataset DOI:** https://doi.org/10.21227/n3jg-ww46

The dataset contains annotated images of five consumer brands:

- Colgate  
- Dettol  
- Classmate  
- Kellogg’s  
- Himalaya  

### Dataset characteristics

- 344 images (300 train, 30 validation, 14 test)
- COCO JSON annotations
- 640 × 640 resolution
- Realistic retail shelf environments
- Multi-brand scenes and cluttered layouts

Images were obtained through a combination of author-collected supermarket photographs and publicly accessible online sources.

---

## Repository Contents
├── Brand_Detection_Notebook.ipynb  
├── map_plot.png (generated)  
├── per_class_ap.png (generated)  
└── README.md  


---

## Methodology

The notebook implements:

- COCO-format dataset loader
- Faster R-CNN with ResNet-50 FPN backbone
- Training with stochastic gradient descent
- Evaluation using COCO mAP@0.5 metric
- Per-class AP computation
- Visualization of predictions
- Inference on held-out test image

---

## Requirements

Recommended environment:
python >= 3.9
torch
torchvision
numpy
matplotlib
opencv-python
pycocotools
Pillow

1. Download dataset

Download from IEEE DataPort and extract:

Brand Detection Dataset/  
 ├── train/  
 ├── valid/  
 └── test/  
 
2. Update dataset path
Modify the BASE variable inside the notebook:
BASE = "path/to/Brand Detection Dataset"  

3. Run notebook

Execute cells sequentially to:
Train model
Generate mAP plot
Produce per-class metrics
Run inference visualization

## Results

The notebook reports:
Validation mAP@0.5
Per-class AP@0.5  
Training curves
Example detection outputs
These results demonstrate dataset usability for multi-class retail product detection research.

## Reproducibility

The repository is archived through Zenodo to ensure long-term reproducibility and citation.

## Citation

If you use this work, please cite:
Brand Detection Dataset, IEEE DataPort, DOI: 10.21227/n3jg-ww46

## License

This repository is released under the MIT License.
The dataset is provided for non-commercial research and educational use.
