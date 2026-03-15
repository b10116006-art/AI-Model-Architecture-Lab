# Vision Transformer Representation Experiment

## Objective

This experiment investigates how different token aggregation strategies affect classification performance in Vision Transformers.

---

## Dataset

CIFAR100

---

## Original Method

Class Token Representation

In the original Vision Transformer architecture, the [CLS] token is used as the representation of the entire image.

---

## Modified Method

Patch Mean Pooling

Instead of using the class token, we compute the average of all patch embeddings.
