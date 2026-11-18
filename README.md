# U-Net: Convolutional Networks for Biomedical Image Segmentation

### NumPy Implementation From Scratch

A complete implementation of the U-Net architecture using **NumPy**, without relying on deep learning frameworks such as PyTorch or TensorFlow.

This project is based on the original research paper:

**Ronneberger, O., Fischer, P., and Brox, T. (2015).**  
*U-Net: Convolutional Networks for Biomedical Image Segmentation.*

---

## Project Overview

U-Net is a convolutional neural network designed for biomedical image segmentation. It uses an encoder-decoder architecture with skip connections to combine contextual information and precise localization.

The objective of this project is to understand and implement the main components of U-Net from scratch using NumPy, including forward propagation, backpropagation, training, and image segmentation.

## Architecture

The implementation includes:

- Contracting path (Encoder).
- Expansive path (Decoder).
- Skip connections with center cropping.
- Convolutional layers (3×3 and 1×1).
- ReLU activation.
- Max Pooling (2×2).
- Up-Convolution (2×2).
- Dropout.
- He weight initialization.

## Main Features

- U-Net implementation from scratch using NumPy.
- Manual forward and backward propagation.
- Numerical gradient verification.
- Pixel-wise Softmax and weighted Cross-Entropy loss.
- Elastic deformation and data augmentation.
- SGD optimizer with momentum (0.99).
- Overlap-tile inference strategy.
- Test-time augmentation using four rotations.
- Image segmentation evaluation.

## Dataset

The notebook uses a **synthetic Electron Microscopy (EM)-like dataset by default**:

- 30 training images.
- 5 test images.
- Image resolution: 256 × 256.
- Two classes: Cells and Membranes.

The notebook also includes an optional loader for the real ISBI 2012 dataset.

## Technologies

- Python
- NumPy
- Matplotlib
- SciPy
- Jupyter Notebook

## Installation

Clone the repository:

```bash
git clone https://github.com/fouzia4/UNet-From-Scratch.git
cd UNet-From-Scratch
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

## How to Run

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `unet_numpy_from_scratch.ipynb` and execute the cells sequentially.

## Evaluation Metrics

The implementation evaluates segmentation using:

- Pixel Error
- Rand Error (simplified)
- Intersection over Union (IoU)

## Project Structure

```text
UNet-From-Scratch/
│
├── README.md
├── requirements.txt
└── unet_numpy_from_scratch.ipynb
```

## Limitations

The default experiment uses synthetic data and a reduced U-Net configuration (8 base channels and 1,200 training iterations).

Therefore, its results should not be directly compared with the original paper's reported results on ISBI 2012.

## References

Ronneberger, O., Fischer, P., & Brox, T. (2015).

U-Net: Convolutional Networks for Biomedical Image Segmentation.

https://arxiv.org/abs/1505.04597

---

**Author:** Fouzia Outmani  
**Field:** Artificial Intelligence and Applications (Master IAA)
