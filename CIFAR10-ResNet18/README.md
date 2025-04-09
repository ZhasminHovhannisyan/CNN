# Transfer Learning: CIFAR-10 Classification with ResNet18

This project is an example of a CNN Fine-Tuning. **ResNet18** network will be trained further to classify images of 
**CIFAR-10 dataset** using PyTorch.

---

##  Dataset

- **CIFAR-10**: 60,000 color images (32x32), 10 classes
- Split: 50,000 training, 10,000 testing
- Classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck

---

##  Model

- Backbone: **ResNet18**
- Modifications:
  - Fully connected head adapted for 10 output classes
  - **Staged unfreezing** of layers during training
  - Varying **learning rates per stage**
- Optimizer: Adam 
- Loss: CrossEntropyLoss

---

##  Training Strategy

- **Staged Unfreezing**:
  - Start by training only the classifier
  - Gradually unfreeze lower layers
  - Apply lower learning rates to earlier layers
- **Checkpoints** and **confusion matrices** are saved every 3 epochs

---

##  Evaluation

- Metrics:
  - **Accuracy**
  - **Loss curves**
  - **Confusion matrix**
  - **Per-class precision & recall**
- Final accuracy: 96% on test set

---

##  Visualizations

-  Training vs. Validation Loss
-  Accuracy Curve
-  Confusion Matrix
-  Per-Class Performance

---


