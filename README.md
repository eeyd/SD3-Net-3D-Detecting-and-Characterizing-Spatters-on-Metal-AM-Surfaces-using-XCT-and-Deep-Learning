# SD3-Net: 3D Detecting and Characterizing Spatter Particles on Metal Additively Manufactured Surfaces using X-Ray Computed Tomography and Deep Learning

This repository contains the implementation of **SD3-Net**, a 3D deep learning framework designed for spatter-particle detection using X-ray Computed Tomography (XCT) volumetric data. The method bridges XCT-based metrology with data-driven analysis for quality assurance in metal additive manufacturing (AM).

> **Note:** As this project is supported by Agency for Science, Technology and Research (A\*STAR) and Industry Alignment Fund – Pre-Positioning Programme (IAF-PP), the release of model weights and datasets is subject to approval. They will be made available here once approved.
---

## 🔍 **Overview**

SD3-Net includes:
- 3D spatter particle dataset and labelling
- 3D Volumetric patch classification
- 3D voxel-level spatter detection and segmentation  
- XCT and 3D deep learning pipeline for spatter detection
---

## 📦 **Repository Structure**

- **SD3-Net/**
  - **sd3net/** — Model architecture and network components  
    - `model.py` — SD3-Net architecture
    - best_sd3net.pth` — Best model weights, selected based on the validation dataset.
  - **utils/** — Data loading, preprocessing, and evaluation tools  
    - `dataloader.py`  
    - `preprocess.py`  
    - `metrics.py`  
  - **scripts/** — Training and inference scripts  
    - `train.py`  
    - `infer.py`  
  - **configs/** — YAML configuration files  
    - `train.yaml`  
  - **data/** — 3D spatter data and labelling
  - **results/** — Sample outputs and visualizations  
  - `requirements.txt` — Python dependencies  
  - `README.md` — Project documentation  

## 3) Data Format:

- **Images:** 16-bit TIF format.

- **Masks:** Binary 8-bit TIF  
  - `0` = background  
  - `255` = foreground  
  - Same name and same size as the corresponding image.
