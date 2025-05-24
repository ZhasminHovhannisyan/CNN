# YOLO object detection on Pascal VOC

---

## Introduction
 
This project is an example of fine-tuning YOLO11m object detection model on the 
Pascal VOC dataset. 
The workflow includes converting VOC annotations to YOLO format, 
splitting into train/val/test, 
setting up a custom dataset, 
training with frozen backbone and mixed-precision, 
and evaluating results with training curves.

---

## Project Structure
```
├── inference/ 
│   ├── models                            # same model with different size and inference time 
│   │   ├── yolo11m-finetune.engine       # TensorRT int8 quantization, GPU speedup 
│   │   ├── yolo11m-finetune.onnx         # speedup for CPU
│   │   └── yolo11m-finetune.pt           # Standard format for model inference 
│   ├── webcam-script.py                  # Streamlit demo script
│   ├── yolo11m-finetune.csv              # Metrics logged per epoch
│   └── README.md                         # Guide on using Streamlit
├── YOLO-obj-det-PascalVOC.ipynb
└── README.md                             # Project documentation
```

---

## Details
No need to install the dataset or any dependencies. Everything is packaged in this single [notebook](YOLOv11-obj-det-PascalVOC.ipynb), eliminating the need for any external files or manual setup steps.

In the [inference](inference/) directory you can find [detailed explanation](inference/README.md) on how to inference demos via Streamlit.

## Clone the repo and enter this project's folder
```
git clone https://github.com/ZhasminHovhannisyan/CNN.git
cd CNN/YOLOv11-Obj-Det-PascalVOC
```

