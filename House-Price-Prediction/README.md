# Housing Price Prediction with Neural Networks

This project builds a **regression model using PyTorch** 
to predict housing prices based on various structured features.
The workflow includes preprocessing, model training with 
early stopping and learning rate scheduling, and
visualization of results.

---

## Dataset

The dataset contains **545 rows** of housing data with the following features:

- Numerical: `area`, `bedrooms`, `bathrooms`, etc.
- Binary categorical: `mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`, `prefarea` (converted to 0/1)
- One categorical column: `furnishingstatus` (encoded with one-hot)
- Target variable: `price` 
- 
---

## Data Preprocessing

The data is preprocessed using the following steps:

1. **Convert binary columns** (`yes`/`no`) into 0 and 1.
2. **One-hot encode** the `furnishingstatus` column.
3. **Cap outliers** in the price column at the 95th percentile to reduce skew.
4. **Apply log transform** on the target (`price`) to normalize its distribution.
5. **Scale features and target** using `StandardScaler`.
6. **Split** into training and testing sets (80/20 ratio).

---

## Neural Network Architecture

- Input layer: Size determined by input_size (number of features)
- Hidden layer 1: 256 neurons with ReLU activation and 50% dropout
- Hidden layer 2: 128 neurons with ReLU activation and 30% dropout
- Output layer: 1 neuron (for regression output)
- Forward Pass: Data flows through fully connected layers (fc1, fc2, fc3), with ReLU activations adding non-linearity and dropout preventing overfitting
---

## Training

The model is trained with:

- **MSE loss**
- **Adam optimizer**
- **Learning rate scheduler** (`ReduceLROnPlateau`)
- **Early stopping** (patience = 20 epochs)



## Evaluation and Summary

After training, we evaluate on the test set:

- Predictions and targets are **inverse transformed** from log and scaling.
- Evaluation metrics:
  - **Test MSE** on original price scale
  - **R² Score**: ~0.70

This means the model explains approximately **70% of the variance** in unseen housing prices.


>  The model has reasonable generalization without severe overfitting (Train Loss: 0.3085, Test Loss: 0.5639)
---

## Future Work

Possible improvements can be made:

- Try ensemble models like **XGBoost** or **LightGBM**
- Perform **hyperparameter tuning** (layers, LR, batch size)
- Add **feature interactions** and **domain-specific insights**
- Use **cross-validation** for more robust evaluation

---
