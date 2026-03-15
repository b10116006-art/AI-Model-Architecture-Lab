# Vision Transformer Representation Experiment

## Objective

This experiment investigates how different token aggregation strategies affect classification performance in Vision Transformers.

---

## Dataset

CIFAR100

---

## Original Method

Class Token Representation

In the original Vision Transformer architecture, the `[CLS]` token is used as the representation of the entire image.

---

## Modified Method

Patch Mean Pooling

Instead of using the class token, we compute the average of all patch embeddings.

x = mean(x[:,1:,:], dim=1)

---

## Results

Top-1 Accuracy

0.3288 → 0.3670

Top-5 Accuracy

0.6074 → 0.6432

---

## Key Insight

Averaging all patch embeddings provides a richer global representation compared to relying on a single class token.
