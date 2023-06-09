---
title: More Information
weight: 4
---

## Starting point

We provide code to generate sample data for the Challenge datasets:

**Dataset 1**: [GitHub LIDCI-IDRI Data](https://github.com/XRad-Ulm/E2MIP_LIDCI-IDRI_data)

Furthermore, we provide baseline implementations for the Challenge tasks:

**Task 1**: [GitHub LIDCI-IDRI Classification](https://github.com/XRad-Ulm/E2MIP_LIDCI-IDRI_classification)

**Task 2**: [GitHub LIDCI-IDRI Segmentation](https://github.com/XRad-Ulm/E2MIP_LIDC-IDRI_segmentation)

**Task 3**: [GitHub Fetal Brain Segmentation](https://github.com/Faghihpirayesh/E2MIP_Challenge_FetalBrainSegmentation)


These solutions provide a straightforward baseline and should help to prepare own solutions. They can also serve as a starting point for individual development, but a completely new design is possible and encouraged.

Right now, the baseline implementations are missing the containerizing scripts. As the evaluation system is currently set up, we didn’t want to share a solution that might have to be changed again. As soon as the system is finalized and tested, a template containerizing script will be provided. 

## Evaluation

The evaluation of submissions will consider both the algorithm's performance and energy efficiency, as we anticipate that there will be a trade-off between the two. To avoid a bias towards a particular aspect, we will jointly evaluate them, allowing for more energy-efficient solutions if performance is less critical and vice versa for more performance-critical applications.

We will not name a specific winner for each task but will use a Pareto-front to evaluate all approaches. Submissions will be displayed in a diagram with both aspects as axis labels. A solution will be on the Pareto-front when there is no other solution that performs better while showing the same or better energy efficiency.

To ensure that all submissions are still usable, we require a minimum performance of 80% of the baseline approaches and allow a maximum time for training and inference. Training and inference for each submission will be conducted on a high-performance computing node with 4 NVIDIA A100 GPUs (each with 48 GB VRAM) and an Intel Xeon Platinum 8368 processor. Task 1 and Task 2 have a maximum runtime of 4 days, while Task 3 has a maximum runtime of 7 days.

The key metrics for performance evaluation will be the Area under ROC-Curve for classification and Dice Similarity Coefficient for segmentation. Energy consumption will be measured by the system's hardware. Example code the calculation of performance metrics is included in the baseline implementations. 

## Submission Process

Each submission requires three aspects to be considered. Please read this in advance to make sure that all information is gathered.

1. A script to create the container that includes the training and inference phases.
2. A paper that describes the submitted solution and possibly includes a preliminary analysis.
3. A complete answer to the submission questions. These include:
   - Basic organization questions like name and affiliation of team members.
   - A Survey on the development process, including questions on the training procedures, any external data used for pre-training, the estimated run-time of all experiments.
   
Please make sure to roughly track the development process in order to be able to answer all questions, especially point 3b.

The submission process will be done via CMT3, the same system that is used for MICCAI submissions. The link to the submission page will be communicated here. 

## Challenge Publication 
A summary publication in a leading journal describing the findings from the challenge is envisioned after the challenge. Successful teams are invited to contribute to the paper. The number of coauthors per team will be decided later depending on the number of submissions. We aim for at least two co-authors per team.
