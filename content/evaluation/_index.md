---
title: Evaluation
weight: 6
---

The evaluation of submissions will consider both the algorithm’s performance and energy efficiency, as we anticipate that there will be a trade-off between the two. To avoid a bias towards a particular aspect, we will jointly evaluate them, allowing for more energy-efficient solutions if performance is less critical and vice versa for more performance-critical applications.

## 📏 Evaluation criteria
The energy consumption of each submission will be measured with an in-build hardware measurement of the underlying system. The training and the inference phase will be measured and reported independently. 

The key metrics for the performance evaluation of the algorithms will be the Area under ROC-Curve for classification and Dice Similarity Coefficient for segmentation. Energy consumption will be measured by the system’s hardware. Example code the calculation of performance metrics is included in the baseline implementations.

## 📈 Ranking
No ranking will be produced for the challenge, to account for the possible trade-off between energy and performance and encourage creative approaches. Instead a Pareto-front will be reported for each task to evaluate all approaches. Submissions will be displayed in a diagram with energy used as on axis and performance as the second axis. A solution will be on the Pareto-front when there is no other solution that performs better with a lower energy consumption.


