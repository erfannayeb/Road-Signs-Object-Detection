# Object Detection with YOLOv5

## About The Project
This repository contains code for training and evaluating an object detection model using YOLOv5 on the road signs dataset.
  
## Dataset
The road signs dataset used for this project contains images of various road signs belonging to the following 4 classes: traffic lights, stop signs, speed limit signs, and crosswalks. The dataset is small and contains only 877 images in total.

## Approach
  ### Training: 
  - To train the YOLOv5 model on the road signs dataset, run the following command:
      - python train.py --data data.yaml --cfg yolov5s.yaml --weights '' --batch-size 16
  ### Evaluation: 
  - To evaluate the YOLOv5 model on the road signs dataset, run the following command:
      - python test.py --data data.yaml --weights runs/train/exp/weights/best.pt --batch-size 16
  ### Inference: 
  - To perform object detection on an image using the trained YOLOv5 model, run the following command:
      - python detect.py --source path/to/image.jpg --weights runs/train/exp/weights/best.pt

## Requirements
- Python
- Numpy
- Pandas
- PyTorch 
