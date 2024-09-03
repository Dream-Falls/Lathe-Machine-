# Lathe Machine Parts Detection
<a href="https://universe.roboflow.com/dreamfalls/ml-project-mwqxv">
    <img src="https://app.roboflow.com/images/download-dataset-badge.svg"></img>
</a>
 <a href="https://colab.research.google.com/github/Dream-Falls/Lathe_Machine/blob/main/Source_Code.ipynb" target="_parent\"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

This project aims to detect four specific parts (obj1, obj2, obj3, and obj4) of a lathe machine present in the workshop of Medicaps University. The project involves collecting real images, annotating them, and training a YOLOv8x model to accurately identify these parts.

## Project Overview

The goal of this project was to develop a robust detection model for identifying four key parts of a lathe machine in a workshop environment. The process involved collecting images, preprocessing them, and using state-of-the-art object detection techniques.

## Dataset

- **Original Images:** 251 real images of the lathe machine were captured in the workshop.
- **Annotation:** Images were annotated in the required format using [Roboflow](https://roboflow.com/).

  
- **Preprocessing:**
  - **Auto-Orient:** Applied to standardize the orientation of images.
  - **Resize:** Fit images within 640x640 pixels using reflect edges.
  - **Augmentations:**
    - **Brightness:** Adjusted between -19% and +19%
    - **Blur:** Applied up to 2.5px
    - **Bounding Box Augmentations:**
      - **Brightness:** Between -19% and +19%
      - **Blur:** Up to 1.5px

- **Final Dataset Size:** 603 images
  - **Training Set:** 528 images
  - **Validation Set:** 25 images
  - **Test Set:** 50 images

## Model

- **Model Used:** [YOLOv8x](https://ultralytics.com/yolov8) by Ultralytics
- **Pretrained Model:** The `yolov8x.pt` pretrained model was fine-tuned for 25 epochs on the dataset.
- **Hardware Requirement:** A GPU is essential for training the model efficiently due to the computational complexity involved in fine-tuning.

## Results

- **Precision:** 0.9350
- **Recall:** 0.7827
- **mAP@50:** 0.8981
- **mAP@50-95:** 0.6212

## Conclusion

This project successfully demonstrates the ability to detect and classify parts of a lathe machine using the YOLOv8x model. The results indicate high precision and recall, making the model suitable for deployment in similar workshop environments.



