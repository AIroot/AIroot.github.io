---
layout: post
title: Predictive Wine Quality System
date: 2017-04-12 00:00:00 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: redwine.jpg # Add image post (optional)
tags: [Decision Tree, Random Forests] # add tag
---
Used 4898 wine data set to create a model to predict the wine quality. Trained the model using Decision Trees and Random Forests algorithms.

## [{Source Code DT-CART}](https://github.com/AIroot/Machine-Learning-Projects-with-R/blob/master/Decision_Trees_Algorithm/DT_Wine_Quality/DTWineQualityCART.R)

## [{Source Code DT-C50}](https://github.com/AIroot/Machine-Learning-Projects-with-R/blob/master/Decision_Trees_Algorithm/DT_Wine_Quality/DTWineQualityC50.R)

## [{Source Code RF}](https://github.com/AIroot/Machine-Learning-Projects-with-R/blob/master/Random_Forests_Algorithm/RF_Wine_Quality/RFWineQuality.R)

### Decision Trees 

#### Objective: Predict the wine quality using decision trees.

A decision tree is a classifier that partitions data recursively into to form groups or classes. This can be used in discrete or continuous data for classification or regression. The Algorithm used in the decision trees are ID3 , C4.5, CART, C5.0, CHAID, QUEST, CRUISE, etc.
This project Use C5.0 algorithm and CART for Wine quality data set.

### Data Visualizatio


![]({{site.baseurl}}/assets/img/Predictive_wine_quality_system/image3.png)

Figure 01: bar chart for quality levels 

According to the above figure 01, there are a lot of wines with a quality of 6 as compared to the others. The dataset description states  that there are a lot more normal wines than excellent or poor ones. For the purpose of this project, let’s classify the wines into good, bad, and normal based on their quality.


![]({{site.baseurl}}/assets/img/Predictive_wine_quality_system/image5.png)

Figure 02: Decision tree 

![]({{site.baseurl}}/assets/img/Predictive_wine_quality_system/image7.png)


Figure 03: Histogram (Grid view) 


![]({{site.baseurl}}/assets/img/Predictive_wine_quality_system/image9.png)


Figure 04: Alcohol vs quality 

What is the accuracy of your tree model?
C5.0(Without Boosting) accuracy is 0.8625

![]({{site.baseurl}}/assets/img/Predictive_wine_quality_system/image8.png)


### Boosting the accuracy of decision trees

This is a process in which many decision trees are built and the trees vote on the best class for each example. The C5.0() function makes it easy to add boosting to our C5.0 decision tree and it  needs to add an additional trials parameter indicating the number of separate decision trees to use in the boosted team.


C5.0 With boosting accuracy is 0.8875

![]({{site.baseurl}}/assets/img/Predictive_wine_quality_system/image2.png)



#### Recursive partitioning trees accuracy without pruning = 0.8469

The recursive portioning tree includes two main processes:

01. recursion

02. partitioning.  

![]({{site.baseurl}}/assets/img/Predictive_wine_quality_system/image1.png)

According to the above results it can be concluded that C5.0 has more accuracy than rpart().

### Random Forests 

### Objective: Predict the wine quality using random forests.


The random forest output notes that it included 500 trees and tried number of three variables at each split. out-of-bag error rate is 13.76%

![]({{site.baseurl}}/assets/img/Predictive_wine_quality_system/image6.png)

Accuracy is 0.8938

![]({{site.baseurl}}/assets/img/Predictive_wine_quality_system/image10.png)


What is the result compared to decision trees and random forests? 
Decision tree accuracy C5.0 = 0.8625
Decision tree accuracy C5.0 with boosting = 0.8875
Decision tree accuracy rpart = 0.8469
Random forest accuracy = 0.8938
The decision tree with  C5.0 has error rate 14%. but with boosting it will reduced to 11.25% . But Random forest provides more accuracy model by reducing  error rate to 10.62%.  



![]({{site.baseurl}}/assets/img/Predictive_wine_quality_system/image4.png)


### References

Lantz, B. (2013). Machine Learning with R. Packt Publishing Ltd.

UCI Machine Learning Repository: Wine Quality Data Set. (n.d.). Retrieved Aprial 4, 2017, from https://archive.ics.uci.edu/ml/datasets/wine+quality

Yu-Wei, C. (2015). Machine Learning with R Cookbook. Birmingham, England: Packt Publishing.

