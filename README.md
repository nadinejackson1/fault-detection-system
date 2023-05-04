# Fault Detection System 

This project implements a fault detection system using a Convolutional Neural Network (CNN) to detect and eliminate faulty products based on their shape and color. The project is part of the GRIP (Graduate Rotational Internship Project) tasks for the IoT and Computer Vision Internship at The Sparks Foundation.

### Table of Contents

- **Introduction**
- **Installation**
- **Dataset Preparation**
- **Model Training**
- **Model Evaluation**
- **Usage**
- **License**

### Introduction

This fault detection system uses the Caltech 101 dataset, which contains images of objects belonging to 101 categories. We use a subset of categories to simulate faulty and non-faulty products. The system is implemented using TensorFlow and Keras.

### Installation

1. Clone this repository:

    git clone https://github.com/nadinejackson1/fault-detection-system.git

### Dataset Preparation

1. Download the [Caltech 101 dataset from here](https://data.caltech.edu/records/mzrjq-6wc02) and extract the contents.

2. Prepare the dataset by running **prepare_dataset.py**. This script selects a few categories from the dataset to represent non-faulty and faulty products, and splits the dataset into training and testing sets.

### Model Training

1. Train the model using the prepared dataset by running **train_model.py**. 

3. This script defines the CNN model, compiles it, and trains it using data augmentation. After training, the model is saved as **fault_detection_model.h5**.

### Model Evaluation

1. Evaluate the model on the test dataset by running **evaluate_model.py**. This script loads the trained model and calculates its accuracy on the test set.

### Usage

Use the **predict_fault.py** script to predict whether a product is faulty or non-faulty based on an input image. Provide the path to the image and the path to the trained model as arguments.

    python predict_fault.py --image_path path/to/image.jpg --model_path fault_detection_model.h5

### License

This project is licensed under the MIT License. See the LICENSE file for details.
