---
title: "Details"
weight: 2
header_menu: true
---

&nbsp;

### Challenge Outline and Datasets
The challenge consists of different based on two datasets, allowing the evaluation of optimization ideas on different tasks. While we encourage everyone to submit solutions for the different tasks, this is optional.

Two datasets are used for this challenge. Their complementary nature allows for assessing different aspects of the development phase.

- A private dataset (The Boston Child Dataset). XXX (Describe the dataset here. ) 
- A public dataset (The LIDC dataset) XXX (Describe the dataset here)

The solutions have to be submitted as a script that generated a container which then includes the final solution. The script will be executed by the organizers to create the target containers. The container will then be run on a high-performance system which allows for tracking the energy consumption. There is no limitation w.r.t to the technology that can be used, as long as it is possible to run inside the container and all custom code is readable to the organizers to allow for rule checking. For more details on the requirements see the rule section. 


---

### Tasks
This year, the following tasks will be evaluated. 

##### Task 1: Classification of a known dataset
The objective is to predict the malignancy of lung nodules based on CT images, with segmentations of each nodule already being provided. The entire dataset is available to participants, reflecting the standard development process.
To tackle this task, participants must submit their untrained solutions, which will then be trained and evaluated on an unknown data split. As such, the submitted solution must contain both the training process and the inference process. Non-learning-based solutions may opt for an empty training process.
The submitted solutions will be evaluated on their classification performance and energy consumption during both the training and inference phases.

##### Task 2: Segmentation of a known dataset
The objective is to segment lung nodules based on CT images. The entire dataset is available to participants, reflecting the standard development process.
To tackle this task, participants must submit their untrained solutions, which will then be trained and evaluated on an unknown data split. As such, the submitted solution must contain both the training process and the inference process. Non-learning-based solutions may opt for an empty training process.
The submitted solutions will be evaluated on their segmentation performance and energy consumption during both the training and inference phases.

##### Task3
The goal is to segment XXX in slices of 3D MR images. The dataset is mainly unknown to the participants, only exemplary images are available.
To solve this task, the participants have to submit their untrained solution. The solution will then be trained and evaluated on the final training- and test-dataset. Since the original dataset is not available, the submitted solution must not only contain any training and the inference process but also the final hyperparameter tuning. An empty training process is possible for non-learning-based solutions. 
The solution will be evaluated w.r.t to classification performance as well as energy consumption during hyperparameter tuning with training and inference. 



---

### Starting point
Baseline solutions are available for each task. The code for task 1 and task 2 can be found in this repository, while the code for task 3 is given here. 

These solutions provide a straightforward baseline. It can be used to help to prepare own solutions or serve as a starting point for individual developments. Of course, their own solutions are encouraged. 


---

### Submission Process
Each submission requires three aspects to be considered. Please read this in advance to make sure that all information is gathered.  

1. A script to create the container that includes the training and inference phase. 
2. A paper that describes the submitted solution and possibly includes a preliminary analysis. 
3. A complete answer of the submission questions. These include:
   - Basic organization questions like name and affiliation of team members 
   - A Survey on the training process. Asking for estimates aspects like the number of training runs, the data usage during training, the estimated run-time for all experiments. 

Please make sure to roughly track the development process in order to be able to answer all questions, especially point 3b.  


---
### Rules

#### Submitted solutions
- The participants should submit a script that creates a container containing everything necessary for the training and inference. 
- A internet connection is available for the creation of the container, but not during training or inference. 
- The organizers might check the submitted code to ensure abides to the rules. The submitted solutions should allow for that. However, the submitted solution does need to be publicly available but might be secured, for example by a password given in the code. 
- No side information about the data should be used, i.e. no hard coding of cases, no pretraining on the datasets etc… 
- Pretrained models might be used if they are:
  - Not trained on the challenge data. 
  - Not made solely for the challenge. 
  - Publicly available and well-documented.
  
  In question, the organizers will decide if a model can be used. Please reach out if you are unsure. 
- Each team can submit one solution per task  to allow the execution of all submissions in a short time frame. Adaptations are possible if enough resources can be allocated. 

#### Submitted Paper
- Each team should submit a paper along the final solution in order to participate in the challenge. 
- The paper should follow the good scientific practice. 
- The paper should be sufficient to reproduce the submitted solution. 
- The paper should explain the main ideas used for the final contribution. 
- We encourage adding preliminary evaluation results to the submitted paper. 
- We strongly encourage the discussion of the development process, of ideas that didn’t work out or were inferior. 
- Participants are welcome to publish their results after the challenge in any venue, however, there is an embargo on the official results from the challenge until the challenge paper is published. 
- Teams related to the organizers can contribute to the challenge but will be highlighted as such.

#### Participation teams
- A team can either consist of a single individual or multiple persons. 
- Each individual can only be part of a single team. 
- Due to legal restrictions, it is not possible to participate for persons with affiliations to organizations in countries that are on the current embargo list for HPC from the USA or EU. If you think this might apply to you, please contact the organizers. 


---
### Challenge Publication 
A summary publication describing the findings from the challenge is envisioned after the challenge. We envision the publication in a leading journal and successful teams are invited to contribute to the paper. The number of coauthors per team will be decided later depending on the number of submissions, we aim for at least two coauthors per team.  


---
### Evaluation
The evaluation will consider two aspects: the algorithm’s performance and energy efficiency. We see both as related and think that there is a trade-off. To avoid a focus on a certain aspect, we will jointly evaluate them. This allows picking more energy-efficient solutions if the performance is less critical and vice versa for more performance-critical applications. 

Consequently, we will not name a specific winner for each task but use a Pareto-front to evaluate all approaches. The submissions will be shown in a diagram with both aspects as axis labels. A solution is on the Pareto-front when there is no other solution that performs better while showing the same or better energy efficiency.  

To ensure that all submissions are still usable, we require a minimum performance of 80% of the baseline approaches and allow a maximum time for training and inference.

Training and inference of each submission will be conducted on a HPC node with 4 NVIDIA A100 GPUs (each 48 GB VRAM) and a Intel Xeon Platinum 8368 processor. For task 1 and task 2, a maximum runtime of 4 days is allowed, and for task 3 a maximum of 7 days. 

The key metrics for performance evaluation will be Area under ROC-Curve for classification and DICE for segmentation. The energy consumption will be used as measured by the system’s hardware. 


---
### Timeline
The challenge is currently open. 

Submission date is the 17th of September. Late submissions might be possible, but we cannot guarantee the execution of the submission
