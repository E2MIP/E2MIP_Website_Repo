---
title: More Information (?)
weight: 4
---

## More Information (?)


### Starting point
Baseline solutions are available for each task. The code for task 1 and task 2 can be found in this repository, while the code for task 3 is given here. 

These solutions provide a straightforward baseline. It can be used to help to prepare own solutions or serve as a starting point for individual developments. Of course, their own solutions are encouraged. 

### Submission Process
Each submission requires three aspects to be considered. Please read this in advance to make sure that all information is gathered.  

1. A script to create the container that includes the training and inference phase. 
2. A paper that describes the submitted solution and possibly includes a preliminary analysis. 
3. A complete answer of the submission questions. These include:
   - Basic organization questions like name and affiliation of team members 
   - A Survey on the training process. Asking for estimates aspects like the number of training runs, the data usage during training, the estimated run-time for all experiments. 

Please make sure to roughly track the development process in order to be able to answer all questions, especially point 3b.  

### Challenge Publication 
A summary publication describing the findings from the challenge is envisioned after the challenge. We envision the publication in a leading journal and successful teams are invited to contribute to the paper. The number of coauthors per team will be decided later depending on the number of submissions, we aim for at least two coauthors per team.  

### Evaluation
The evaluation will consider two aspects: the algorithm’s performance and energy efficiency. We see both as related and think that there is a trade-off. To avoid a focus on a certain aspect, we will jointly evaluate them. This allows picking more energy-efficient solutions if the performance is less critical and vice versa for more performance-critical applications. 

Consequently, we will not name a specific winner for each task but use a Pareto-front to evaluate all approaches. The submissions will be shown in a diagram with both aspects as axis labels. A solution is on the Pareto-front when there is no other solution that performs better while showing the same or better energy efficiency.  

To ensure that all submissions are still usable, we require a minimum performance of 80% of the baseline approaches and allow a maximum time for training and inference.

Training and inference of each submission will be conducted on a HPC node with 4 NVIDIA A100 GPUs (each 48 GB VRAM) and a Intel Xeon Platinum 8368 processor. For task 1 and task 2, a maximum runtime of 4 days is allowed, and for task 3 a maximum of 7 days. 

The key metrics for performance evaluation will be Area under ROC-Curve for classification and DICE for segmentation. The energy consumption will be used as measured by the system’s hardware. 