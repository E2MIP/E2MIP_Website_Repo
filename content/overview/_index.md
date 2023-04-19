---
title: Challenge Overview
weight: 2
---

## Outline and Datasets
The challenge consists of different based on two datasets, allowing the evaluation of optimization ideas on different tasks. While we encourage everyone to submit solutions for the different tasks, this is optional.

Two datasets are used for this challenge. Their complementary nature allows for assessing different aspects of the development phase.

- A private dataset (The Boston Child Dataset). XXX (Describe the dataset here. ) 
- A public dataset (The LIDC dataset) XXX (Describe the dataset here)

The solutions have to be submitted as a script that generated a container which then includes the final solution. The script will be executed by the organizers to create the target containers. The container will then be run on a high-performance system which allows for tracking the energy consumption. There is no limitation w.r.t to the technology that can be used, as long as it is possible to run inside the container and all custom code is readable to the organizers to allow for rule checking. For more details on the requirements see the rule section.



## Tasks

This year, the following tasks will be evaluated. 

### Task 1: Classification of a known dataset
The objective is to predict the malignancy of lung nodules based on CT images, with segmentations of each nodule already being provided. The entire dataset is available to participants, reflecting the standard development process.
To tackle this task, participants must submit their untrained solutions, which will then be trained and evaluated on an unknown data split. As such, the submitted solution must contain both the training process and the inference process. Non-learning-based solutions may opt for an empty training process.
The submitted solutions will be evaluated on their classification performance and energy consumption during both the training and inference phases.

### Task 2: Segmentation of a known dataset
The objective is to segment lung nodules based on CT images. The entire dataset is available to participants, reflecting the standard development process.
To tackle this task, participants must submit their untrained solutions, which will then be trained and evaluated on an unknown data split. As such, the submitted solution must contain both the training process and the inference process. Non-learning-based solutions may opt for an empty training process.
The submitted solutions will be evaluated on their segmentation performance and energy consumption during both the training and inference phases.

### Task 3
The goal is to segment XXX in slices of 3D MR images. The dataset is mainly unknown to the participants, only exemplary images are available.
To solve this task, the participants have to submit their untrained solution. The solution will then be trained and evaluated on the final training- and test-dataset. Since the original dataset is not available, the submitted solution must not only contain any training and the inference process but also the final hyperparameter tuning. An empty training process is possible for non-learning-based solutions. 
The solution will be evaluated w.r.t to classification performance as well as energy consumption during hyperparameter tuning with training and inference. 
