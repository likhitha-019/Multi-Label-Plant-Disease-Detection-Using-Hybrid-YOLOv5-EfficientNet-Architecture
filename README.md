🌱 Multi-Label Plant Disease Detection Using Hybrid YOLOv5-EfficientNet Architecture

A cutting-edge multi-label plant disease detection system that intelligently combines
YOLOv5 (🟦 spatial localization) and EfficientNet-B2 (🟩 semantic understanding) — enhanced with
dual-channel attention, disease co-occurrence modeling, and specialized multi-label loss functions.

This hybrid architecture delivers real-time inference, multi-disease detection, and
is fully optimized for web apps, mobile devices, and edge hardware.

🔍 Project Highlights

✨ YOLOv5 + EfficientNet-B2 Hybrid Model
🎯 Multi-Label Classification — detects multiple plant diseases in a single image
🧠 Attention Mechanisms — Channel + Spatial attention refinement
🔗 Disease Co-Occurrence Matrix — reduces contradictory predictions
⚖️ Custom Loss Function — Focal Loss + Asymmetric Loss
⚡ Real-Time Inference — 15 FPS on NVIDIA Tesla T4
📱 Mobile Ready — 140 MB FP16 model + quantization support
🌾 27 Real-World Disease Classes
🏆 Achieved F1-Score: 89.2% (macro)

📷 System Overview
🟦 YOLOv5 Backbone — Spatial Intelligence

Detects where disease symptoms appear

Multi-scale feature maps

Trained on MS COCO

Handles variable lesion size, shape, and position

🟩 EfficientNet-B2 Backbone — Semantic Intelligence

Extracts what disease is present

Strong generalization from ImageNet pretraining

Lightweight + high accuracy

🔀 Feature Fusion Layer

Multi-level fusion of YOLOv5 + EfficientNet feature maps

1×1 convolution for dimensional consistency

Enhances both localization & classification

🎛️ Dual-Channel Attention Module

Channel Attention → focuses on important feature channels

Spatial Attention → highlights disease-affected leaf regions

Boosts F1-score by +1.2% in ablation studies

🔗 Disease Co-Occurrence Matrix

Learnable 27×27 matrix

Learns real-world disease pairing patterns

Eliminates contradictory predictions (reduced 15% → 3%)

📂 Dataset Used
🌿 PlantDoc Dataset (Real-World Agricultural Images)

A challenging dataset of field-captured plant disease images, containing:

2,598 images

27 diseases & healthy classes

Tomato 🍅

Potato 🥔

Pepper 🌶️

Field variations: uneven lighting, cluttered background, leaf occlusion

🔧 Dataset Split

80% Training

10% Validation

10% Testing
(maintaining label distribution)

🧪 Data Augmentation

🔄 Rotation (±30°)

↔️ Flips

🎨 Color Jitter (HSV, brightness, contrast)

🧩 Mosaic Augmentation

🔗 MixUp Augmentation

📏 Normalization (ImageNet Mean/Std)
