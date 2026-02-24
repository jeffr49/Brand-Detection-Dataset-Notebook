[![DOI](https://zenodo.org/badge/1163455168.svg)](https://doi.org/10.5281/zenodo.18725821)
# Brand-Detection-Dataset-Notebook

## Overview

This repository provides the training and evaluation notebook for the **Product Brand Detection dataset**, a multi-class object detection dataset designed for recognizing consumer product brands in retail environments.

The notebook demonstrates end-to-end experimentation including dataset loading, model training, evaluation using COCO metrics, per-class performance analysis, and inference visualization.

---

## Dataset

**Dataset DOI:** [10.21227/n3jg-ww46](https://doi.org/10.21227/n3jg-ww46)

The dataset contains 344 images (300 train, 30 validation, 14 test) at $640 \times 640$ resolution, featuring realistic retail shelf environments for five brands:

* **Colgate**
* **Dettol**
* **Classmate**
* **Kellogg’s**
* **Himalaya**

---

## Methodology

The notebook utilizes a **Faster R-CNN** model with a **ResNet-50-FPN** backbone. The implementation includes:

* **COCO-format** dataset loader.
* Training via **Stochastic Gradient Descent (SGD)**.
* Evaluation using **mAP@0.5** and per-class AP computation.

---

## Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Brand-Detection-Dataset-Notebook.git
cd Brand-Detection-Dataset-Notebook

```

### 2. Install Requirements

Ensure you have Python $\ge$ 3.9 installed. Use the provided `requirements.txt` to set up your environment:

```bash
pip install -r requirements.txt

```

### 3. Download the Dataset

Download the files from **IEEE DataPort** and extract them into your project directory:

```text
Brand Detection Dataset/
 ├── train/
 ├── valid/
 └── test/

```

### 4. Configure & Run

Update the `BASE` variable in the notebook to point to your local dataset path:

```python
BASE = "path/to/Brand Detection Dataset"

```

Execute the cells in `Brand_Detection_Notebook.ipynb` sequentially to train and evaluate the model.

---

## Repository Contents

```text
├── Brand_Detection_Notebook.ipynb  # Main training/eval notebook
├── requirements.txt               # Project dependencies
├── map_plot.png                   # Generated mAP curves
├── per_class_ap.png               # Per-class performance metrics
└── README.md                      # Documentation

```

## Results

The notebook generates training curves, validation mAP@0.5, and visual inference examples on held-out test data, demonstrating the feasibility of multi-brand detection in cluttered retail scenes.

## Citation

If you use this work, please cite:

> *Brand Detection Dataset, IEEE DataPort, DOI: 10.21227/n3jg-ww46*

## License

This repository is released under the **MIT License**. The dataset is provided for non-commercial research and educational use.

---
