AUTHORS:
Ludwig Wideskär (luai18@student.bth.se),
Akshaya Bathula (akba21@student.bth.se)


CONTENTS OF THIS FILE
---------------------

* Description
* Requirements
* Installation
* How it works
* Testing
* Results


DESCRIPTION
-----------
The aim of our work for the assignment is to select three supervised classification algorithms and compare their 
predictive and computational performance.It is compared based on three criterions: 
1. Computational performance in terms of training time. 
2. Predictive performance based on accuracy. 
3. Predictive performance based on F-measure. 


REQUIREMENTS
------------
The following requirements is needed for the program to run:

* Spambase dataset must be present within the same folder
* Python intrepreter

The following Python modules needs to be installed on the system:
* numpy
* matplotlib
* pandas
* sklearn
* datetime
* tabulate
* array


INSTALLATION
------------
Upload the files to Google Colab or use a similar online jupyter service.
Make sure that all the requirements are fulfilled.
You are now ready to run the program.

HOW IT WORKS
------------
The Spambase dataset is used to compare the three selected algorithms and their performance. Spambase contains 4600
entries of either positive or negative result of email spam.To minimize generalization errors in the result, 
training and testing of the classifying algorithms are using stratified k-fold cross-validation, with the function
Kfold from the sklearn model selection library, against the dataset. Main comparison between the selected algorithms
is done by using a Friedman test for each criterion.

In the stratified ten-fold cross-validation test the data is split in to 10 equal parts and tested with the 3 
selected algorithms. The average, standard deviation of these 3 algorithms is also calculated. 

TESTING 
-------
If the Friedman test indicates that there is a significant difference between two or more algorithms, then a Nemenyi
test is also done to conclude which algorithm is significantly better than the other or others. 
In the Friedman test the three relevant variables: average rank, sum of squared differences(second quantity) and 
sum of squared differences(third quantity) are calculated. If the significant difference is greater than the 
critical value the null hypothesis is rejected and nemenyi test is calculated. 
In the nemenyi test the significant difference is calculated as the friedman test shows that the selected algorithms
perform the same. 

RESULTS
--------
The 1. Computational performance in terms of training time, , and the difference between them is calculated for the selected 
algorithms. The results show that:
1. For the Computational performance in terms of training time
Null hypothesis was rejected. Nemenyi test is needed. 
The algorithm K-NN performs significantly better than SVM with a performance difference of 
2.0. 

2. For the Predictive performance based on accuracy
Null hypothesis is rejected. Nemenyi test is needed. 
The algorithm K-NN performs significantly better than Naive Bayes with a performance difference of 2.0.

3. For the Predictive performance based on F-measure is calculated 
Null hypothesis is rejected. Nemenyi test is needed. 
The algorithm K-NN performs significantly better than Naive Bayes with a performance difference of 2.0.