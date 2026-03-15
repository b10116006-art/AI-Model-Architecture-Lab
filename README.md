# AI Model Architecture Lab

Author: Po-Yun Chen

This repository documents a series of deep learning experiments exploring how architectural changes influence model performance.

Instead of only running course notebooks, this project focuses on **systematically modifying model architectures and analyzing experimental results**.

The experiments cover two major model families used in modern computer vision:

- Convolutional Neural Networks (CNN)
- Vision Transformers (ViT)

---

# Experiments

This lab currently contains two architecture experiments.

| Experiment | Architecture | Dataset |
|------|------|------|
CNN Backbone Replacement | ResNet50 → ResNet18 | Oxford Pet |
Vision Transformer Representation | Class Token vs Patch Mean | CIFAR100 |

---

# Experiment 1 — CNN Backbone Replacement

Goal: Replace a large CNN backbone (ResNet50) with a smaller backbone (ResNet18) and evaluate performance differences.

Result:

| Model | Validation Accuracy |
|------|------|
ResNet50 | 0.9212 |
ResNet18 | 0.9234 |

Observation:

ResNet18 achieved comparable accuracy despite having significantly fewer parameters, suggesting that smaller backbones can still extract sufficient visual features for certain tasks.

---

# Experiment 2 — Vision Transformer Representation Strategy

Goal: Evaluate different image representation strategies in Vision Transformers.

Original method:
x = x[:,0]


Modified method:


x = x[:,1:,:]
x = torch.mean(x, dim=1)


Result:

| Representation | Top-1 | Top-5 |
|------|------|------|
Class Token | 0.3288 | 0.6074 |
Patch Mean | 0.3670 | 0.6432 |

Observation:

Aggregating patch embeddings improved classification accuracy, suggesting that combining information from all image patches can produce a richer representation than relying solely on the class token.

---

# Skills Demonstrated

- PyTorch model modification
- CNN backbone replacement
- classifier head adaptation
- Vision Transformer architecture understanding
- representation learning strategies
- experimental comparison and analysis

---

# Future Work

Future experiments may include:

- Vision Transformer attention visualization
- CNN vs Transformer performance comparison
- lightweight transformer architectures
- hybrid CNN–Transformer models
