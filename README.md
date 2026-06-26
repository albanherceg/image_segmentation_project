# Semantic Image Segmentation using Deep Learning

A university project comparing three state-of-the-art semantic segmentation models on the Oxford-IIIT Pet Dataset.

## Overview

The goal of this project was to compare the performance of different convolutional neural network architectures for semantic image segmentation.

The following models were implemented and evaluated:

- U-Net
- PSPNet
- DeepLabV3+

Each model was trained using both **Cross Entropy Loss** and **Dice Loss**, then evaluated using the **mean Intersection over Union (mIoU)** metric.

---

## Dataset

The models were trained on the **Oxford-IIIT Pet Dataset**, which contains:

- 37 dog and cat breeds
- RGB images
- Pixel-wise segmentation masks (trimaps)

The dataset was split into training, validation and test sets.

---

## Training Configuration

- Framework: PyTorch
- Optimizer: AdamW
- Image size: 128 × 128
- Batch size: 8
- Learning rate: 3e-3
- Epochs: 12

### Data Augmentation

- Horizontal Flip
- Shift, Scale & Rotate
- Brightness / Contrast adjustment
- Hue & Saturation adjustment
- Gaussian Noise

---

## Evaluation Metric

The models were evaluated using **Mean Intersection over Union (mIoU)**, one of the most widely used metrics for semantic segmentation tasks.

---

## Results

| Model | Cross Entropy | Dice Loss |
|--------|--------------:|----------:|
| U-Net | 0.796 | **0.796** |
| PSPNet | 0.764 | 0.771 |
| DeepLabV3+ | 0.792 | **0.796** |

### Observations

- Dice Loss consistently achieved equal or better performance than Cross Entropy Loss.
- U-Net achieved the highest overall segmentation accuracy.
- DeepLabV3+ provided the best balance between accuracy and computational efficiency.
- PSPNet converged more slowly and would likely benefit from higher-resolution inputs or longer training.

---

## Technologies

- Python
- PyTorch
- NumPy
- Albumentations
- Matplotlib
- Google Colab

---

## Repository Structure

```
.
├── notebook.ipynb
├── presentation.pdf
├── README.md
├── requirements.txt
└── images/
```

---

## Future Improvements

Possible extensions of this project include:

- Higher image resolution
- More training epochs
- Larger datasets
- Combined loss functions
- Ensemble methods

---

## Authors

This project was developed as part of a university Deep Learning course by a team of three students.

**My contributions included:**

- Model implementation
- Training and experimentation
- Performance evaluation
- Result analysis
- Project documentation
