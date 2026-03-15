# CNN Backbone Replacement Experiment

## Objective
This experiment investigates the effect of replacing the CNN backbone architecture.

The original model used ResNet50 as the backbone.
In this experiment, we replace it with ResNet18 and evaluate the classification performance.

---

## Dataset

Oxford-IIIT Pet Dataset

This dataset contains images of cats and dogs across multiple breeds.

---

## Model Architecture

CNN-based image classification model.

Architecture:

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

## Modification

Original backbone:
ResNet50

Modified backbone:
ResNet18

ResNet18 is a lighter architecture with fewer parameters and faster training time.

---

## Results

Training completed successfully with stable convergence.

The experiment demonstrates that a smaller backbone can still achieve competitive performance while reducing model complexity.

---

## Key Insight

Backbone architecture plays a critical role in feature extraction.

Even lightweight architectures like ResNet18 can produce strong feature representations for classification tasks.

---

## Results

Validation Accuracy

ResNet50: 0.9212  
ResNet18: 0.9234

---

## Key Insight

Replacing a larger backbone with a lighter architecture can still preserve strong classification performance.

In this experiment, ResNet18 achieved comparable and slightly better validation accuracy while reducing model complexity and improving training efficiency.
