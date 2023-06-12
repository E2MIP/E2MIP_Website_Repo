---
title: Challenge Overview
weight: 2
---

## Outline
The Energy-Efficient Medical Image Processing challenge consists of three tasks based on two datasets. A participating team may address only one or two of the tasks, but we encourage everyone to submit solutions for all three tasks.

The solutions have to be submitted as a script that generates a container which then includes the final solution. The script will be executed by the organizers to create the target containers which will then be run on a high-performance computational system with the capability to monitor and record the energy consumption. There is no limitation w.r.t to the technology that can be used, as long as it is possible to run inside the container, and all custom code is readable to the organizers to allow for rule checking. Of course, the task must be solved by relying on the provided training/test data without incorporating additional knowledge about the dataset during inference. For more details on the requirements, please see the Rules section.

## Datasets
Two datasets are used for this challenge. Their complementary nature allows for assessing different aspects of the development phase.

### Dataset 1 (Lung Nodule) 
Here, the public LIDC-IDRI dataset will be used. It contains more than 1.000 CT images of patients with lung nodules. All images have been annotated by experts with segmentations (for nodules > 3mm) and a malignancy rating. The corresponding publications give a detailed description of the dataset ([10.7937/K9/TCIA.2015.LO9QL9SX](https://doi.org/10.7937/K9/TCIA.2015.LO9QL9SX) , [10.1118/1.3528204](https://doi.org/10.1118/1.3528204) )
The dataset can be downloaded from the [The Cancer Imaging Archive (TCIA)](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=1966254). Beside the images and annotations, this includes additional description and details of the dataset. 

### Dataset 2 (Fetal brain MRI)
This dataset consists of T2-weighted and diffusion-weighted MRI scans of fetal brains. The brain has been manually segmented by an expert to provide ground truth labels. The dimensions of T2-weighted and diffusion-weighted MRI images, respectively, are 256 x 256 x S and 128 x 128 x S voxels, where S is the number of slices in the scan. In other words, the size of each 2D slice for T2-weighted and diffusion-weighted scans are 256 x 256 and 128 x 128, respectively. The within-slice resolutions vary. Scans are available as NIfTI files (.nii.gz).

## Tasks

### Task 1: Classification of a known dataset (Dataset 1)
The objective is to predict the malignancy of lung nodules based on CT images, with segmentations of each nodule already being provided. The entire dataset is available to participants, reflecting the standard development process. To tackle this task, participants must submit their untrained solutions, which will then be trained and evaluated on an undisclosed data split. As such, the submitted solution must contain both the training process and the inference process. Non-learning-based solutions may opt for an empty training process. The submitted solutions will be evaluated based on their classification performance and energy consumption during both the training and inference phases.

### Task 2: Segmentation of a known dataset (Dataset 1)
The objective is to segment lung nodules on CT images. The entire dataset is available to participants, reflecting the standard development process. To tackle this task, participants must submit their untrained solutions, which will then be trained and evaluated on an undisclosed data split. As such, the submitted solution must contain both the training process and the inference process. Non-learning-based solutions may opt for an empty training process. The submitted solutions will be evaluated based on their segmentation performance and energy consumption during both the training and inference phases.

### Task 3: Segmentation of an unknown dataset (Dataset 2)
For this task, the dataset is not disclosed to the participants. Only a few examples are provided in order to give the participants a sense of how the data look like. The objective is to segment the fetal brain in MRI slices.
To solve this task, the participants have to submit their untrained solution. The solution will then be trained and evaluated on the final training and test data samples. Since the dataset is not disclosed, the submitted solution must include any hyperparameter tuning that the participating teams may wish to implement. Needless to say, the energy usage for such hyperparameter tuning will be counted towards the total energy usage. Therefore, methods that can reach high segmentation accuracy with little hyperparameter tuning will be advantageous. An empty training process is possible for non-learning-based solutions.
