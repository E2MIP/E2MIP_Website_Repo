---
title: Submission
weight: 7
---

Submissions must provide a docker that will be run on local hardware to ensure a fair and comprehensive assessment of the required energy. For learning-based solutions, the final training run must be included in the docker file, non-learning based may opt for an empty training process. 

Additional details on the submission process (Homepage, requirements, how-to’s and docker template) will be provided here in future. 

## 🗳️ Submission 

The submissions are handled using the CMT3 system that is also used for the main MICCAI conference. Here, you can submit both the describing paper as well as the code using a link or a zip file. 

**[Submission page on CMT](https://cmt3.research.microsoft.com/E2MIP2024)**

If you want to participate by submitting solutions to more than one task we recommend to create multiple submissions, one for each tasks. While this is not mandatory, it really simplifies to identify the correct solutions for each task. The submitted paper that describes the process can be the same for all tasks.  

## 📦️ Docker 
A containerized solution is required for the submission of each solution. Once build, the container must not require any internet connetion in order to train or interfer the results. Consequently any package installation, model downloading etc.. should be done while creating the corresponding container. 

### Docker template

You might use our [template docker file](/data/Dockerfile) as a starter and adapt it to your need. A different dockerfile might also be used on your own risk. 

**[Template Dockerfile](/data/Dockerfile)**

### Container requirements

The container could be either a docker container or an [enroot](https://github.com/NVIDIA/enroot) container. As a submitted docker container will be convert into an enroot container to run on our systems, we would prefer an enroot container. However, knowing that most people are more familiar with docker, we also allow docker containers that will then be transformed to enroot container by us.

For training, the following directories will be mounted: 
* **/mnt/training_data** : A folder containing the training data, including the original images and the ground truth
* **/mnt/training_results** : A folder that is accessible both during training and inference, can be used to store trained parameters.
For training, we will call the script /submission/train.sh . This script can also simply execture an single python command. 

For inference, the following directories will be mounted: 
* **/mnt/training_results** : A folder that is accessible both during training and inference, can contain the trained models.
* **/mnt/query_data** : A folder containing the data for which the inference/predicting should be done
* **/mnt/predicted_data** : The folder to which the predictions should be saved. 
For training, we will call the script /submission/inference.sh . This script can also simply execture an single python command. 

### Input / Output format

The data to be used by the container will be in the same format as the data it is used in the [code examples](/code_examples/). 

For the LIDC-IDRI-based tasks, this means that: 
* **Input data format:** The data will be processed according to the preprocessing script from the code examples.
* **Data loader:** You can use the data loader given in the LIDC examples if you want to, but this is not mandatory. 
* **Storing classifcation results:** For each nodule, the predictions should be stored in an individual file at the path testing_data_prediction_classification/scan_<SCANID>/nodule_<NoduleID>.txt with <SCANID> and <NoduleID> being the ID of the scan and the nodules resprectively. The file should contain the probabilities for each class in a comma (,)-separated way. 
* **Storing segmentation results:** The results of the segmentation task should be stored in a file at the location testing_data_prediction_segmentation/scan_<SCANID>/prediction_total.nii", with SCANID being the ID of the individual scan. Each file should contain the segmentation of the whole image. 
* **Example evaluation code:** A example code for the evaluation is given in the repositories of the code examples for both LIDC-IDRI tasks. If you can evaluate your solution using this code, it should also work with our solution. 

The details about the provided and expected file format for the fetal brain segmentation task is given in the repository of the example solution.