# 🚘 License Plate Detection Using YOLO11

A lightweight **Computer Vision object detection system** for detecting license plates from vehicle images using **YOLO11n**.

The project focuses on establishing a strong baseline using a publicly available license plate detection dataset and evaluating the model on a held-out test set.

---

## 📌 Project Overview

License plate detection is an important component of **Automatic License Plate Recognition (ALPR/ANPR)** systems.

This project implements a simple detection pipeline:

```text
Input Image
     ↓
YOLO11n
     ↓
License Plate Detection
     ↓
Bounding Box + Confidence Score
```

The current version focuses specifically on **license plate detection**. OCR-based license number recognition is outside the scope of this baseline.

---

## 🎯 Objectives

* Train a YOLO11-based license plate detector.
* Evaluate detection performance on an unseen test set.
* Measure Precision, Recall, F1 Score, and mAP@50.
* Build a simple image-based prediction system.
* Establish a baseline for future improvements and domain-specific fine-tuning.

---

## 🧠 Model

**Model:** YOLO11n

YOLO11n was selected because it provides a good balance between:

* Detection performance
* Inference speed
* Computational efficiency
* Ease of deployment

The model was fine-tuned using a publicly available license plate detection dataset.

---

## 📊 Dataset

**Dataset:** License Plate Recognition Dataset

**Source:** Roboflow Universe

**Dataset Version:** v11

**Images:** 10,125

**Task:** Object Detection

**Annotation Format:** YOLOv11

The dataset contains annotated license plate bounding boxes from vehicle images.

> The dataset itself is not included in this repository. Please refer to the original dataset source and its license/usage terms before downloading or using it.

---

## ⚙️ Training Configuration

| Parameter      |            Value |
| -------------- | ---------------: |
| Model          |          YOLO11n |
| Epochs         |               50 |
| Image Size     |        640 × 640 |
| Batch Size     |               16 |
| Task           | Object Detection |
| Dataset Format |          YOLOv11 |

The best-performing checkpoint was automatically selected based on validation performance.

---

## 📈 Test Set Results

The trained model was evaluated on the dataset's held-out test set.

| Metric        |      Score |
| ------------- | ---------: |
| **Precision** | **99.03%** |
| **Recall**    | **94.56%** |
| **F1 Score**  | **96.75%** |
| **mAP@50**    | **96.95%** |

### Interpretation

* **Precision — 99.03%:** The model produces very few false-positive detections.
* **Recall — 94.56%:** The model detects the majority of actual license plates.
* **F1 Score — 96.75%:** Indicates a strong balance between precision and recall.
* **mAP@50 — 96.95%:** Shows strong object detection performance at an IoU threshold of 0.50.

> These results represent performance on the public dataset's test set and should not be interpreted as Bangladesh-specific real-world performance.

---

## 📁 Repository Structure

```text
license-plate-detection-yolo11/
│
├── notebook/
│   └── License_Plate_Detection_YOLO11.ipynb  
│
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

The original dataset is intentionally excluded from this repository.

---

## 🛠️ Technologies

* Python
* PyTorch
* Ultralytics YOLO11
* Roboflow
* Google Colab
* Computer Vision
* Object Detection

---

## 🚀 Future Work

Possible future improvements include:

* Evaluation on Bangladesh-specific vehicle images
* Bangladesh license plate dataset creation
* Fine-tuning with local road scenes
* Detection under low-light and motion-blur conditions
* Motorcycle-specific plate detection analysis
* Real-time video detection
* License plate image enhancement
* OCR integration for automatic plate number recognition
* Complete end-to-end ANPR system

Future pipeline:

```text
Vehicle Image / Video
        ↓
License Plate Detection
        ↓
Plate Cropping
        ↓
Image Enhancement
        ↓
OCR
        ↓
License Number Recognition
```

---

## ⚠️ Limitations

This project currently performs **license plate detection only**.

It does not:

* Read or recognize the characters on the plate.
* Perform vehicle tracking.
* Provide Bangladesh-specific validation.
* Guarantee performance under unseen geographic or environmental conditions.

The reported metrics are based on the selected public dataset and its test split.

---

## 📚 Dataset & References

* Roboflow Universe — License Plate Recognition Dataset
* Ultralytics YOLO11

Please follow the original dataset and model licenses when using this project.

---

## 👤 Author

**Md Delwar Husen**

Machine Learning & Computer Vision Enthusiast

Interested in:

* Machine Learning
* Deep Learning
* Computer Vision
* Medical AI
* AI Research

---

## ⭐ Project Status

**Status:** Baseline Completed ✅

The initial YOLO11n model achieved:

**99.03% Precision | 94.56% Recall | 96.75% F1 | 96.95% mAP@50**
