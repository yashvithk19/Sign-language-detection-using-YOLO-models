# Sign Language Detection using YOLO Models

## Overview
This project implements Sign Language Detection using four different versions of YOLO (You Only Look Once) object detection models:
- YOLOv5-Large (YOLOv5l)
- YOLOv5-Medium (YOLOv5m)
- YOLOv8-Large (YOLOv8l)
- YOLOv8-Medium (YOLOv8m)

The models are trained and tested on the **American Sign Language (ASL) dataset** to detect and recognize various hand signs.

## Dataset
The **American Sign Language (ASL) dataset** consists of images representing different hand signs. The dataset is preprocessed and annotated to be used for object detection tasks with YOLO models.

## Project Structure
```
📂 Sign-Language-Detection-using-YOLO-models
│── 📂 dataset               # Dataset with its labelled annotations
│── 📂 models-info           # Detailed Description of implemented YOLO models
│── 📂 implementation        # .py files for code references
│── 📂 results               # result for inference, evaluation and comparation
│── 📄 README.md             # Project documentation
```

## Installation
To set up the environment, install the required dependencies:
```bash
pip install -r requirements.txt
```

## Training the Models
To train a YOLO model on the ASL dataset, use the following command:
```bash
python train.py --model yolov5m --epochs 50 --data asl.yaml
```
Replace `yolov5m` with `yolov5l`, `yolov8m`, or `yolov8l` depending on the model you want to train.

## Inference
To run inference on an image or video, use the following command:
```bash
python detect.py --model yolov8l --source path/to/image_or_video
```
Replace `yolov8l` with the model you want to use.

## Results & Comparisons
The performance of each model is evaluated using metrics such as:
- **mAP (Mean Average Precision)**
- **Confusion Matrix**
- **Accuracy**
- **Various other graphs**
For more info., Refer Results folder.

## Future Work
- Implementing **the same work on video dataset**.

---
For any queries or collaborations, feel free to reach out!

