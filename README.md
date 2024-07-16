Forman Ignite: Machine Learning
Unleash Innovation and Fuel the Future with Foreman Ignite: The Ultimate Machine Learning Showdown.
Overview: 
The task is to use a multi-class approach to predict the outcomes of patients with cirrhosis. Good luck!

Evaluation:
Submissions are evaluated using the multi-class logarithmic loss. Each id in the test set had a single true class label, Status. For each id, you must submit a set of predicted probabilities for each of the three possible outcomes, e.g., Status_C, Status_CL, and Status_D.

The metric is calculated

logloss=−1N∑i=1N∑j=1Myijlog(pij),
where N
 is the number of rows in the test set, M
 is the number of outcomes (i.e., 3),  log
 is the natural logarithm, yij
 is 1 if row i
 has the ground truth label j
 and 0 otherwise, and pij
 is the predicted probability that observation i
 belongs to class j
.

The submitted probabilities for a given row are not required to sum to one because they are rescaled prior to being scored (each row is divided by the row sum). In order to avoid the extremes of the log function, predicted probabilities are replaced with max(min(p,1−10−15),10−15)
.

Submission File
For each id row in the test set, you must predict probabilities of the three outcomes Status_C, Status_CL, and Status_D . The file should contain a header and have the following format:

id,Status_C,Status_CL,Status_D
7905,0.628084,0.034788,0.337128
7906,0.628084,0.034788,0.337128
7907,0.628084,0.034788,0.337128
etc.
Citation
Shoaib Rashid. (2024). Forman Ignite: Machine Learning. Kaggle. https://kaggle.com/competitions/ml-ignite
