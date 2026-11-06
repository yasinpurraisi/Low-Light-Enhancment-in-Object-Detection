# Low-Light Image Enhancement for Object Detection

**Bachelor's Project — Yasin Pourraisi**

## Overview

Object detection is an important task in computer vision, allowing machines to identify and locate objects in images. However, detecting objects in low-light environments can be challenging due to poor visibility, reduced contrast, and image noise.

This project investigates the impact of low-light image enhancement techniques on object detection performance. It also explores whether training an object detection model specifically on low-light images can improve its accuracy.

The project uses the **ExDark dataset** and the **YOLOv8n** object detection model to evaluate different approaches.

## Objectives

- Evaluate object detection performance on low-light images.
- Investigate the effectiveness of different image enhancement techniques.
- Compare enhanced images with the original low-light images.
- Fine-tune an object detection model using low-light data.
- Analyze and compare the results of different approaches.

## Methods

The project evaluates the following approaches:

- **Baseline:** Using a pretrained YOLOv8n model directly on the original low-light images.
- **Gamma Correction:** Improving image brightness through intensity adjustment.
- **CLAHE:** Enhancing local contrast to make image details more visible.
- **Zero-DCE:** Using a deep learning-based method for low-light image enhancement.
- **SCI:** Applying a lightweight deep learning-based image enhancement method.
- **Fine-tuning:** Training YOLOv8n on the ExDark dataset to improve its performance in low-light conditions.

## Dataset

The project uses the **ExDark (Exclusively Dark)** dataset, a dataset specifically designed for object detection in low-light environments.

It contains 7,363 images across 12 object categories, including:

- Bicycle
- Boat
- Bottle
- Bus
- Car
- Cat
- Chair
- Cup
- Dog
- Motorbike
- People
- Table

## Results

The experimental results show that traditional and deep learning-based image enhancement methods did not improve the performance of the pretrained object detection model in this experiment.

However, fine-tuning YOLOv8n on the ExDark dataset significantly improved detection performance.

| Method | mAP@50 | mAP@50–95 |
|---|---:|---:|
| Baseline | 0.4813 | 0.2590 |
| Gamma Correction | 0.4102 | 0.2148 |
| CLAHE | 0.4128 | 0.2202 |
| Zero-DCE | 0.2941 | 0.1522 |
| SCI | 0.2975 | 0.1534 |
| Fine-tuned YOLOv8n | **0.7170** | **0.4488** |

The fine-tuned model achieved approximately **49% improvement in mAP@50** compared to the baseline model.

These results suggest that adapting the object detection model to low-light data can be more effective than enhancing the images alone.

## Conclusion

This project demonstrates that improving image brightness and contrast does not necessarily lead to better object detection results. The effectiveness of image enhancement depends on how the enhanced images interact with the detection model.

Fine-tuning YOLOv8n on low-light images proved to be the most effective approach among the methods evaluated in this project.

## Author

**Yasin Pourraisi**

Bachelor's Student in Computer Science  
Shahid Bahonar University of Kerman

## Acknowledgements

This project was completed as part of my bachelor's degree in Computer Science under the supervision of Dr. Marjan Koochaki Rafsanjani.

