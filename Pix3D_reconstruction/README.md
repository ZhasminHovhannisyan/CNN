# Single-Image 3D Reconstruction on Pix3D

This project studies the problem of reconstructing the three-dimensional geometry of an object from a single RGB image. The task is approached using deep learning and real-world data from the Pix3D dataset, where each image is paired with a corresponding CAD model. The goal of the system is to predict a 3D point cloud that represents the surface of the object using only one input image.

The reconstruction problem is formulated as point-cloud regression. Given an RGB image, a convolutional neural network extracts visual features, which are then mapped directly to a fixed number of 3D points. This representation avoids voxel discretization and explicit mesh topology while remaining simple and computationally efficient.

---

## Method Summary

The model follows an encoder–decoder design. A ResNet-18 network pretrained on ImageNet is used as the image encoder, with its classification layer removed. The encoder produces a compact global feature vector describing the object in the image. This vector is passed to a fully connected regression head that predicts the 3D coordinates of a fixed-size point cloud.

Training is supervised using point clouds sampled from Pix3D CAD models. Since point clouds are unordered, the model is optimized using the Chamfer Distance, which measures geometric similarity between predicted and ground-truth point sets. Encoder weights are kept frozen to improve stability and reduce overfitting.

---

## Project Structure 

```
project_root/
│
├── checkpoint/
│   └── pointnet_pix3d.pt # Trained model (.pt)
│
├── predictions/
│   ├── *_gt.ply                         # Ground-truth point clouds
│   └── *_pred.ply                       # Model predictions
│
├── 3D_reconstruction_Pix3D.ipynb        # Training and inference implementation
└── README.md                            # Project documentation
```

---

## Training and Inference

Training is performed on the Pix3D dataset using supervised learning. During training, checkpoints are saved so that the model state and loss history can be recovered after interruptions. After training, the best checkpoint is loaded for inference on unseen images.

Inference consists of passing a single RGB image through the network to obtain a predicted point cloud. The output is saved to disk and can be visualized alongside the corresponding ground-truth point cloud.

---

## Evaluation

Model performance is evaluated primarily using Chamfer Distance on a validation split of Pix3D. In addition, an F1-score is computed at a fixed distance threshold to measure surface coverage. Since F1 is sensitive to the chosen threshold and scale, it is reported as a secondary metric, while Chamfer Distance is treated as the main indicator of reconstruction quality.

---

## Results and Limitations

The model successfully reconstructs the overall geometry of objects from a single image, capturing major structural components such as seats, backs, and legs in the case of chairs. While fine-grained surface details are limited due to the fixed number of points and direct regression approach, the reconstructed shapes are geometrically consistent and visually interpretable.