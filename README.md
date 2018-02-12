# Gaussian Anaomoly Detection for Server Computers
An anomaly detection algorithm is implemented to detect anomalous behavior in server computers. Using measures of server throughput, latency of response, and a several other variables, a Gaussian distribution of server behavior is created to identify outliers.
## Overview
The anomoly detection tool was created with two steps. First, a 2-D Guassian model was created in order to visualize the behavior of the server computers, and demonstrate the distribution of their behavior. This model makes it easy to show where the outliers live with respect to the specified probability threshold. The second part of this exercise uses a more realistic feature space consisting of 11 dimensions. For both problems, various thresholds are tested until the best F1 score is achieved.
## Estimating Parameters for a Gaussian
The Guassian model takes as inputs, the mean, and the variance of the dataset. This is performed using estimateGaussian.m. Using ex8.m, a visualization of the 2-D Guassian distribution is created as shown in Figure 2. 

![alt text](https://github.com/edwardsta/gaussian-anomoly-detection/blob/master/Figure2.PNG)

## Selecting the Anomoly Threshold
The threshold for anomoly detection, with respect to the Guassian distribution, is defined using selectThreshold.m. This code calculates the optimal threshold using the F1 score on a cross validation set. Numerous threshold values are tested until the F1 score is optimized. Figure 3 shows a visualization of the classified anomolies for the simple 2-D dataset.

![alt text](https://github.com/edwardsta/gaussian-anomoly-detection/blob/master/Figure3.PNG)
