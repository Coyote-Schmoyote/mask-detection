# Mask detection

Object detection is a computer vision task that is used to identify objects and their location inside an image. Object detection is often confused with image recognition, however, these two tasks are two distinct tasks. Image recognition assigns a label to an image. For example, a picture of a cat receives athe label "cat." Object detection, on the other hand, draws a bounding box around the cat, and labels the box "cat." In other words, object detection algorithm provides more information about hte target image than an image recognirion alogirthm.

Object detection has a number of real-world applications, including crowd counting, self-driving cars, video surveillance, face detection, anomaly detection, etc.

## Object detection with dlib

Dlib has a pre-trained object detector, which already includes some object categories. For this project, we will train a custom object detector by manually creating annotations for our images using imglab and dlib function train_simple_object_detector().

## Problem definition

Build an object detector, which will be able to detect faces with masks, and faces without the masks.

## Data

For this project, we are using a part of the COVID-19 Medical Face Mask Detection Dataset (https://www.kaggle.com/datasets/mloey1/medical-face-mask-detection-dataset). The dataset consists of 1415 images of people wearing face masks. In principle, the more images we use to train our model, the more accurate the results will be. However, with the more images we use, the longer it takes to complete the training. Because of this, it is customary to first test the feasibility of the project by using a fraction of the data.

In this project, we will use 35 images to train the model, 7 annotated images to test the model performance, and 7 images without annotations. In total, we will use 49 images to complete the mask detection project.

## Approach

To build our mask detector, our worflow will include 5 broad steps:

* Tool and data preparation
* Image labeling
* Custom object detector training
* Combining object and face detectors
