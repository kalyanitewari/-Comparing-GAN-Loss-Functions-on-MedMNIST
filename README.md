
# 🔬 GAN Loss Function Comparison on MedMNIST v2

This repository contains an in-depth comparison of different loss functions used in Generative Adversarial Networks (GANs) on the MedMNIST v2 dataset.

## 📌 Objective

To compare the performance of the following GAN loss functions on a medical imaging dataset:
- **LSGAN (Least Squares GAN)**
- **WGAN (Wasserstein GAN)**
- **WGAN-GP (Wasserstein GAN with Gradient Penalty)**

## 🧠 Models Overview

All models use:
- Input: 100-dimensional noise vector
- Output: 28x28 grayscale medical images
- Architecture: Common generator and discriminator
- Framework: PyTorch
- Epochs: 100
- Batch Size: 64

### 🔁 Differences

| Model     | Key Change                        |
|-----------|-----------------------------------|
| **LSGAN** | MSE loss for discriminator        |
| **WGAN**  | Wasserstein loss with weight clipping |
| **WGAN-GP** | Wasserstein loss with gradient penalty |

---

## 🧬 Dataset

**MedMNIST v2** — a lightweight biomedical image classification dataset. The dataset used:
- Grayscale 28x28 images
- Ideal for quick benchmarking of deep learning models
- Downloaded and loaded via `medmnist` API

---

## 🧪 Evaluation Metrics

- **FID (Fréchet Inception Distance)**: Measures similarity to real data distribution
- **Inception Score (IS)**: Measures sample diversity and clarity

Calculated using `torch-fidelity`.

---

## 📊 Results Summary

### 🔢 Metrics

| Model     | FID ↓       | Inception Score ↑ |
|-----------|-------------|-------------------|
| **LSGAN** | ~210.17     | ~1.44             |
| **WGAN**  | ~198.34     | ~1.56             |
| **WGAN-GP** | **~183.42** | **~1.66**         |

### 🖼️ Generated Images

Generated images at the final epoch for each GAN:

> Add output samples here from training logs.

---

## 💡 Key Takeaways

- **WGAN-GP** offers the best visual and metric-based performance.
- Gradient Penalty helps maintain Lipschitz continuity better than weight clipping.
- LSGAN is stable but underperforms in diversity and realism.

---

## 📂 Project Structure

```
.
├── gan-loss-function-comparison.ipynb   # Jupyter Notebook with full experiment
├── README.md                            # GitHub Markdown file
├── results/                             # Sample outputs and evaluation metrics
└── requirements.txt                     # Dependencies
```

---

## 🚀 Run the Notebook

1. Clone the repo:
```bash
git clone https://github.com/your-username/gan-loss-medmnist.git
cd gan-loss-medmnist
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Launch the notebook:
```bash
jupyter notebook gan-loss-function-comparison.ipynb
```

---


## 📬 Contact

Feel free to open an issue or pull request for contributions!

Connect with me on [LinkedIn](https://www.linkedin.com/in/kalyanitewari/) or follow for updates.

---

© 2025 | AI in Healthcare | GAN Loss Function Research
