# 🐾 RF-DETR: Cat and Dog Object Detection (Group 13 - CO2.2 Final Project)

This project implements an object detection system using the *RF-DETR (Receptive Field Enhanced Detection Transformer)* model to detect cats and dogs in images. Built using *PyTorch*, it adapts the transformer-based DETR architecture and enhances it using multi-scale receptive fields for improved object localization.

## 📌 Project Objectives

- Acquire and prepare an annotated image dataset.
- Implement the RF-DETR model with receptive field enhancement.
- Train and evaluate the model using standard metrics: *Accuracy*, *Precision*, *Recall*, *IoU*, and *mAP*.
- Visualize predictions and discuss the model's performance.

---

## 🗃️ Dataset

- *Source*: Roboflow Universe
- *Dataset*: [Dog and Cat Detection](https://universe.roboflow.com)
- *Format*: COCO JSON (bounding box annotations)
- *Splits*:
  - Train: 70%
  - Validation: 15%
  - Test: 15%

---

## 🔧 Model Architecture

- *Backbone*: Custom CNN (configurable)
- *Receptive Field Module*: Multi-kernel convolution layers to enhance feature maps
- *Transformer*: Encoder-decoder structure adapted from DETR
- *Matcher*: Hungarian algorithm for bipartite matching
- *Prediction Heads*: Feedforward networks (FFNs) for class and bounding box predictions

---

## 🏋️‍♂️ Training

- *Optimizer*: AdamW
- *Losses*:
  - Classification loss (CrossEntropy)
  - Bounding box regression (L1)
  - Generalized IoU loss
- *Hyperparameters*:
  - Learning Rate: 1e-4
  - Batch Size: 4
  - Epochs: 30 (adjustable)
- *Features*:
  - Early stopping
  - Model checkpointing

---

## 📈 Evaluation Metrics

- *Accuracy* (for classification)
- *Precision / Recall* (for object detection)
- *IoU* (Intersection-over-Union)
- *mAP@0.5* (Mean Average Precision)

---

## 📊 Visualization

Predicted bounding boxes and class labels are overlaid on test images for visual inspection.

---

## ▶️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/rf-detr-cat-dog.git
cd rf-detr-cat-dog
