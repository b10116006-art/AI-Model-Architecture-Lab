CNN Backbone Replacement Experiment
Objective

This experiment investigates how different CNN backbone architectures affect image classification performance.

Dataset

Oxford-IIIT Pet Dataset

This dataset contains images of cats and dogs across multiple breeds and is commonly used for image classification tasks.

Original Model

ResNet50

ResNet50 is a deeper convolutional neural network architecture with strong feature extraction capability.

Modified Model

ResNet18

ResNet18 is a lighter architecture with fewer parameters and faster training time.

The goal of this experiment is to evaluate whether a smaller backbone can still achieve strong classification performance.

Model Architecture

Input Image
↓
ResNet Backbone
↓
Global Average Pooling
↓
Fully Connected Classifier
↓
Prediction

Results

Validation Accuracy

ResNet50: 0.9212
ResNet18: 0.9234

Key Insight

Replacing a larger backbone with a lighter architecture can still preserve strong classification performance.

In this experiment, ResNet18 achieved slightly higher validation accuracy while reducing model complexity.

This suggests that smaller backbone architectures can be effective for certain classification tasks.
