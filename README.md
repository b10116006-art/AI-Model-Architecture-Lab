# AI Model Architecture Lab

This repository explores fundamental deep learning model architectures used in modern AI systems.

The goal of this project is to experiment with different model design choices and understand how architectural modifications affect performance.

The experiments focus on:

- Convolutional Neural Networks (CNN)
- Vision Transformers (ViT)

---

## Project Overview

This lab documents two computer vision experiments:

1. CNN backbone replacement for image classification
2. Vision Transformer representation strategy comparison

The purpose is not only to run provided notebooks, but to systematically modify model architectures and observe how these changes affect performance.

---

## Experiments

### 1. CNN Backbone Replacement

**Task:** Replace the CNN backbone architecture.

**Original backbone:** ResNet50  
**Modified backbone:** ResNet18

**Dataset:** Oxford-IIIT Pet Dataset

**Goal:** Study how backbone size affects feature extraction and classification performance.

**Experiment folder:** `experiments/cnn-backbone-replacement`

---

### 2. Vision Transformer Representation Strategy

**Task:** Compare two token aggregation strategies in Vision Transformers.

**Original method:** Class Token Representation  
**Modified method:** Patch Mean Pooling

**Dataset:** CIFAR100

**Goal:** Investigate whether averaging all patch embeddings provides better global representation than relying on the class token.

**Experiment folder:** `experiments/vit-representation`

---

## CNN Architecture

![CNN Architecture](assets/CNN architecture with ResNet backbone.png)

This architecture uses a ResNet backbone to extract visual features from images.

**Pipeline:**

Input Image  
↓  
ResNet18 Backbone  
↓  
Global Average Pooling  
↓  
Fully Connected Classifier  
↓  
Prediction

---

## Vision Transformer Architecture

![ViT Architecture](assets/ViT architecture comparison_ pooling strategies.png)

Vision Transformers split images into patches and process them as token sequences using a Transformer encoder.

Two representation strategies are compared:

- Class Token
- Patch Mean Pooling

---

## Vision Transformer Representation Modification

**Original method:**

```python
x = x[:, 0]
```

**Modified method:**

```python
x = x[:, 1:, :]
x = torch.mean(x, dim=1)
```

The modified approach removes the class token and computes the mean representation across all patch embeddings.

---

## Repository Structure

```text
AI-Model-Architecture-Lab
│
├─ assets
│   ├─ CNN architecture with ResNet backbone.png
│   └─ ViT architecture comparison_ pooling strategies.png
│
├─ experiments
│   ├─ cnn-backbone-replacement
│   │   ├─ W1_OxfordPet_Standard_Cross_Entropy.ipynb
│   │   └─ README.md
│   │
│   └─ vit-representation
│       ├─ W1_Vision_Transformer.ipynb
│       └─ README.md
│
└─ README.md
```

---

## Why This Repository Matters

This repository demonstrates practical understanding of:

- CNN backbone replacement
- classifier head implications after changing feature dimensions
- Vision Transformer token aggregation strategies
- experiment design and performance comparison
- PyTorch-based model modification

Rather than only running notebooks, the experiments focus on architecture reasoning, controlled modification, and result interpretation.

---

## Future Work

Future experiments may include:

- Vision Transformer attention visualization
- CNN vs Transformer performance comparison
- lightweight transformer architectures
- hybrid CNN–Transformer models

---

## Author

Po-Yun Chen  
AI × Semiconductor Engineer
