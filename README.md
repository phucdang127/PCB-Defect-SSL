# PCB Assembly Defect Detection Using Supervised and Semi-Supervised Learning

This repository provides representative datasets and source code accompanying our research on PCB assembly defect detection using supervised and semi-supervised object detection methods.

## Repository Contents

The repository contains the following files:

| File | Description |
|------|-------------|
| `Datasets/` | Representative samples of the PCB assembly defect dataset used in this study. |
| `yolo_train_PCB.ipynb` | Training notebook for YOLOv8m and YOLOv11m. |
| `refine_det_train_PCB.ipynb` | Training notebook for RefineDet. |
| `faster_rcnn_train_PCB.ipynb` | Training notebook for Faster R-CNN. |
| `detr_train_PCB.ipynb` | Training notebook for DETR. |
| `transforms.py` | Customized data augmentation functions used in the semi-supervised learning experiments. |
| `wrappers.py` | Wrapper functions implementing the proposed augmentation pipeline. |
| `README.md` | Documentation of this repository. |

---

# Dataset

The `Datasets` directory contains representative annotated samples of the PCB assembly defect dataset used in this work.

Due to industrial confidentiality agreements, the complete dataset cannot be publicly released. The published subset is provided to facilitate reproducibility and demonstrate the dataset organization.

The dataset contains five defect categories:

| Class ID | Defect Category |
|----------|-----------------|
| 0 | Scratches on the circuit board |
| 1 | Scratches on components |
| 2 | Missing/lost component |
| 3 | Damaged component pins |
| 4 | Faulty components |

---

# Supervised Learning

This repository includes the supervised learning models evaluated in the paper.

| Model | Notebook |
|------|----------|
| YOLOv8m | `yolo_train_PCB.ipynb` |
| YOLOv11m | `yolo_train_PCB.ipynb` |
| RefineDet | `refine_det_train_PCB.ipynb` |
| Faster R-CNN | `faster_rcnn_train_PCB.ipynb` |
| DETR | `detr_train_PCB.ipynb` |

These notebooks contain the training configuration and evaluation procedure for each detector.

---

# Semi-Supervised Learning

The semi-supervised learning experiments were implemented based on the following publicly available frameworks.

### Unbiased Teacher

Official implementation:

https://github.com/facebookresearch/unbiased-teacher

### Soft Teacher

Official implementation:

https://github.com/microsoft/SoftTeacher

### Semi-DETR

Official implementation:

https://github.com/PaddlePaddle/PaddleDetection/tree/develop/configs/semi_det/semi_detr

---

# Data Augmentation

The proposed data augmentation strategy used in the semi-supervised learning experiments is implemented in the following files:

- `transforms.py`
- `wrappers.py`

These files contain the customized augmentation pipeline proposed in this work and were integrated into the corresponding semi-supervised learning frameworks.

---

# Environment

The experiments were conducted using:

- Python 3.10+
- PyTorch
- TorchVision
- Ultralytics
- OpenCV
- NumPy
- Matplotlib

Please install the required dependencies for each framework before running the experiments.
