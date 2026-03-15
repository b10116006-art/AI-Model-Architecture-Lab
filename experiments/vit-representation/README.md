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

x = x[:, 1:, :]
x = torch.mean(x, dim=1)


---

## Results

Top-1 Accuracy

0.3288 → 0.3670

Top-5 Accuracy

0.6074 → 0.6432

---

## Key Insight

Averaging all patch embeddings provides a richer global representation compared to relying on a single class token.

This suggests that information distributed across multiple patches can improve classification performance.
