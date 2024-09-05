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

