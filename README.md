# Pipeline Crack detection System using Yolov5

This repository contains a model designed to detect and classify cracks in pipeline images. The model uses YOLOv5 (You Only Look Once), a state-of-the-art real-time object detection algorithm. The project includes training the model using both synthetic pipeline images and real-world data, as well as implementing data augmentation to address overfitting and improve performance.

Project Overview
The goal of this project is to develop a robust model capable of detecting defects (cracks) in pipeline images and classifying them based on their severity (e.g., Minor, Moderate, Severe). The project uses a combination of synthetic data generated with Blender and real-world images to simulate a variety of pipeline defects.

Key Features:
Crack Detection: Detects cracks in pipeline images.
Classification: Classifies cracks into three categories: Minor, Moderate, and Severe.
Synthetic Data Generation: Uses Blender to create realistic pipeline images with synthetic cracks.
Data Augmentation: Augments training data to prevent overfitting and improve model generalization.
YOLOv5 Model: Trains a YOLOv5 object detection model for real-time crack detection.
Evaluation Metrics: Precision, Recall, mAP (mean Average Precision), and Learning Rate plots.

Dataset
The dataset used in this project includes both synthetic pipeline images generated using Blender and real-world images of pipelines with cracks. The dataset is organized as follows:

-Train: Training images and labels.
-Val: Validation images and labels.
-Test: Test images and labels.

The synthetic data is generated using Blender, where cracks are created with different severities and placed in various locations within the pipeline images.

Overfitting Check
If the validation loss is higher than the training loss, and the difference exceeds a threshold, a warning is triggered indicating potential overfitting.

Results
After training the model, the following results were achieved:

Final Epoch: 29
Final Training Box Loss: 0.041008
Final Validation Box Loss: 0.046212
Final Precision: 0.60695
Final Recall: 0.47595
Final mAP@0.5: 0.5168
No significant overfitting detected.
Data Augmentation
Data augmentation is applied during training to improve the model's robustness and reduce overfitting. The following augmentations are used:

Flip: Horizontal and vertical flipping.
HSV: Adjusting hue, saturation, and value.
Scaling and Translation: Random scaling and translation.
Rotation: Random rotation of images.
These augmentations help to simulate various conditions and increase the variability in the training dataset, making the model more generalizable.

Future Work
To further improve the model:

Enhance Synthetic Data: Use Blender to create more diverse and realistic images.
Real-World Data: Collect and annotate real-world pipeline images for better accuracy.
Advanced Regularization: Implement dropout, L2 regularization, and more aggressive data augmentation.
Advanced Models: Experiment with newer object detection models (e.g., YOLOv7, EfficientDet).
Post-Processing: Use Non-Maximum Suppression (NMS) to refine detection results.
Acknowledgments
YOLOv5 for the object detection model.
Blender for generating synthetic pipeline images.
The open-source community for their contributions and research.
License
This project is licensed under the MIT License - see the LICENSE file for details.

