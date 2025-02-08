# Sign Language Detection using YOLO Models

## Overview
This project implements Sign Language Detection using four different versions of YOLO (You Only Look Once) object detection models:
- YOLOv5-Large (YOLOv5l)
- YOLOv5-Medium (YOLOv5m)
- YOLOv8-Large (YOLOv8l)
- YOLOv8-Medium (YOLOv8m)

The models are trained and tested on the **American Sign Language (ASL) dataset** to detect and recognize various hand signs.

## Dataset
The **American Sign Language (ASL) dataset** consists of images representing 26 different hand signs. The dataset is preprocessed and annotated to be used for object detection tasks with YOLO models.

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
For installation and setup, clone the YOLO repository:
```bash
git clone https://github.com/ultralytics/yolov5.git
cd yolov5
```
Replace `yolov5` with `yolov8` depending on the model you want to train.

## Install Dependencies

To train a YOLO model on the ASL dataset, we need to beforehand install the dependencies using the following command:
```bash
pip install ultralytics
```

## Preparing the dataset
Create a data_yaml.yaml file with the dataset structure:
```bash
train: /path/to/dataset/train
val: /path/to/dataset/valid
test: /path/to/dataset/test

nc: 26
names: ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']

```

## Training the model

To train a YOLO model on the ASL dataset, use the following command:
```bash
yolo task=detect mode=train model=yolov5m.pt data=data_yaml.yaml epochs=25 imgsz=640 batch=8 name=desired_name_to_save_file
```
Replace `yolov5m` with `yolov5l` , `yolo8m` or `yolo8l` depending on the model you want to train.


## Results & Comparisons
The performance of each model is evaluated using metrics such as:
- **Confusion Matrix**
- **mAP (Mean Average Precision)**
- **Accuracy**
- **Various other graphs**
For more info., Refer Results folder.

## Future Work
- Implementing **the same work on video dataset**.

---
For any queries or collaborations, feel free to reach out!

