# Vision Transformer Representation Experiment

## Objective

This experiment investigates how different token aggregation strategies affect classification performance in Vision Transformers.

---

## Dataset

CIFAR100

The CIFAR100 dataset contains 100 object classes and is commonly used to benchmark image classification models.

---

## Original Method

Class Token Representation

In the original Vision Transformer architecture, a special `[CLS]` token is appended to the patch tokens.

After passing through the Transformer encoder, the embedding corresponding to the class token is used for classification.

---

## Modified Method

Patch Mean Pooling

Instead of using only the class token, we compute the average of all patch embeddings.

This modification allows the model to use information from every patch.

Implementation:
