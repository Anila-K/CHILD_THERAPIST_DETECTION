
Therapist and Child Detection and Tracking:
==========================================

Project Overview

  This project aims to detect and track children and therapists in videos, using a custom-trained YOLOv8 model to detect persons. The system tracks their movement across the video,         including handling re-entries and occlusion challenges.

Approach
1. Annotation
 
  I annotated 999 frames using Roboflow with two classes:
  Child
  Therapist
2. Model
   
   A custom YOLOv8 model was created and trained using the labeled frames. Two versions of the model were saved based on different epochs:

   Model 1: Trained for 50 epochs.
   Model 2: Trained for 100 epochs.
3. Inference

   The model was tested on the provided test videos, detecting children and therapists. The predictions, including bounding boxes and confidence scores, are saved as output videos.

Project Structure

The folder structure is as follows:

child-therapist-detection/: Contains the labeled images and YAML configuration file used for training the model.
Custom Models/: Contains the trained YOLOv8 models.
model_50_epoch.pt: YOLOv8 model trained for 50 epochs.
model_100_epoch.pt: YOLOv8 model trained for 100 epochs.
output/: Contains the output videos with predictions overlaid.
Model Training.ipynb: Jupyter notebook used for training the YOLOv8 model.
Model Testing.ipynb: Jupyter notebook used for running inference on the test videos.
