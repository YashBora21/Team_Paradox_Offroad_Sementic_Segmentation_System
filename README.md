🚀 Desert Image Segmentation using SegFormer-B2
📌 Overview

This project focuses on semantic segmentation of desert images using a deep learning approach. The goal is to classify each pixel of an image into one of the predefined classes such as sky, landscape, rocks, vegetation, etc.

We use a SegFormer-B2 model combined with advanced training strategies to achieve high accuracy and robust performance under domain shift conditions.

🎯 Objective
Perform pixel-wise classification of desert images
Handle class imbalance effectively
Achieve high IoU (Intersection over Union) score
Build a scalable and efficient segmentation pipeline
🧠 Model Architecture
Encoder: SegFormer-B2 (Transformer-based)
Decoder: Lightweight segmentation head
Key Features:
Multi-head self-attention
Hierarchical feature extraction
Efficient computation for limited GPU
🔄 Pipeline Workflow
1️⃣ Input Preprocessing
Resize images to 512 × 512
Normalize pixel values
Ensure consistent input format
2️⃣ Data Augmentation
Horizontal Flip
Random Crop & Resize
Color Jitter (optimized for desert tones)

➡️ Helps improve generalization and prevent overfitting

3️⃣ Model Training
Model: SegFormer-B2
Loss Function: Weighted Cross-Entropy
Optimizer: AdamW
Learning Rate Scheduler: Cosine Annealing

➡️ Handles class imbalance and improves convergence

4️⃣ Evaluation
Metric: IoU (Intersection over Union)
Per-class IoU analysis
Confusion matrix visualization
5️⃣ Output
Segmentation masks (class-wise)
Colored visualization outputs
Performance metrics


📊 Key Features
✅ Transfer Learning (Pretrained Weights)
✅ Class Imbalance Handling
✅ Efficient GPU Utilization
✅ Early Stopping
✅ Mixed Precision Training
⚙️ Tech Stack
Python
PyTorch
HuggingFace Transformers
OpenCV
NumPy / Matplotlib
💻 Hardware Used
NVIDIA RTX 4070 / Tesla T4 (Colab)
8GB+ VRAM recommended
## 📁 Project Structure

```
desert-segmentation/
├── train.py
├── val.py
├── dataset/
│   ├── train/
│   ├── val/
│   └── test/
├── outputs/
│   ├── predictions/
│   ├── graphs/
│   └── logs/
├── models/
│   ├── segformer_best.pth
│   └── segformer_last.pth
└── README.md
```
▶️ How to Run
1. Install Dependencies
pip install torch torchvision transformers opencv-python matplotlib tqdm
2. Train Model
python train.py
3. Evaluate Model
python val.py
📈 Results
High performance on Sky & Landscape classes
Improved accuracy using weighted loss
Competitive IoU score (~0.53+ and improving)
⚠️ Challenges Faced
Class imbalance (rare objects like logs, clutter)
Domain shift between train and test data
GPU memory limitations
✅ Solutions Implemented
Weighted loss function
Data augmentation
Efficient model architecture
👥 Team

Team Name: Paradox

👨‍💻 Prajwal Barsagade (Leader)
👨‍💻 Yash Bora
👨‍💻 Aditya Sarse



##🏁 Conclusion

This project demonstrates an effective deep learning pipeline for real-world semantic segmentation tasks, especially in challenging environments like desert terrains.

⭐ Future Improvements
Hyperparameter tuning
Better handling of rare classes
Model ensembling
Real-time deployment


