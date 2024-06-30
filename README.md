# Pothole Detection using YOLOv9

![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)
![YOLOv9](https://img.shields.io/badge/YOLOv9-Models-yellow.svg)
![Roboflow](https://img.shields.io/badge/Dataset-Roboflow-orange.svg)

## Overview

Welcome to the **Pothole Detection** project! This repository contains the code and results for detecting potholes using various YOLOv9 models. This project aims to develop an efficient and accurate system for identifying potholes on roads, enhancing safety and maintenance processes.

![Pothole Detection](path_to_sample_image.jpg)

## Table of Contents

- [Dataset](#dataset)
- [Models](#models)
- [Results](#results)
- [Usage](#usage)
- [Installation](#installation)
- [Contributing](#contributing)
- [License](#license)

## Dataset

The dataset used for this project was exported via [Roboflow]( https://public.roboflow.com/object-detection/pothole) and includes 1595 annotated images of potholes in YOLOv8 format. The images underwent the following pre-processing and augmentation steps:
- **Pre-processing**:
  - Auto-orientation of pixel data (EXIF-orientation stripping)
  - Resized to 640x640 (stretch)
- **Augmentation**:
  - Random 90-degree rotations: none, clockwise, counter-clockwise
  - Random crops between 0 and 20% of the image

## Models

We experimented with four different YOLOv9 models:
1. **YOLOv9-s**
2. **YOLOv9-t**
3. **YOLOv9-m**
4. **YOLOv9-c**

Details on each model's architecture, training parameters, and performance metrics can be found in the respective folders.

## Results

The results of the experiments, including precision, recall, and mAP (mean Average Precision) scores, are summarized below:

| Model    | Precision | Recall | mAP@0.5 | mAP@50-95 |
|----------|-----------|--------|---------|---------|
| YOLOv9-s | x.xx      | x.xx   | x.xx    | |
| YOLOv9-t | 0.84623      | 0.71708   | 0.80334    |0.50284|
| YOLOv9-m | x.xx      | x.xx   | x.xx    ||
| YOLOv9-c | x.xx      | x.xx   | x.xx    ||

Detailed results and analysis can be found in the [results](./results) directory.

## Usage

To use the models and reproduce the results, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/pothole-detection.git
   cd pothole-detection
2. **Install dependencies**:
```bash
pip install -r requirements.txt
```
3. **Train the model**:
```bash
python train.py --model yolov9-s --data data/potholes.yaml
```
4.**Evaluate the model**:
```bash
python evaluate.py --model yolov9-s --data data/potholes.yaml
```
