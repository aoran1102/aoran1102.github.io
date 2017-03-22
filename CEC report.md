
## Overview
This internship report is based on my experience as an intern in the California Energy Commission(CEC). During the past three months, I fully used my statistical knowledge and programming skills to deal with the real data. My major goal is to evaluate the potential benefits and risk of the investments of CEC and conducted pressure test for sensitive analysis. Precisely, CEC finances many research projects which aim to develop new technology that could enhance energy saving in California. We quantify energy saving, on-site labor impacts local revenue and supply chain impacts. We also measure different economic impacts given different market permeation and demands. I actively involved in the full cycle of data analysis, collection, cleaning, testing, modeling, visualizing and presenting results to tech/non-tech people to tell them the result. For me, it’s meaningful to help people better understand the business and improve products and services. Overall, I am very satisfied with the accomplishments of my internship. I am more familiar with using my knowledge into practice. I am more confident in my analytical skills. I am more experienced in prioritizing multiple tasks.

## Data Collection 
I primarily focused on using regular expression to get data from the questionnaires. According to the general formats or the formats of words ahead or after the needed information, I created regular expression and used R extract this information. Then, I cleaned the data into a uniform format for further analysis. In other words, I converted responses in the questionnaires into same format. 
We also have different version of questionnaires including questionnaires for kickoff, midterm (several stages based on their starting date and end date) and final to get information about the project. I should clarify the version of questionnaires and combine the information of the same version. 

## Methodology report
This report summarizes the indices and criterion to estimate the benefits. Since the development of technologies, some metrics and criteria are unsuitable to classify good and bad performance so we need to find more appropriate criterion. I conducted literature review including the reports from CEC, the standards of different industries developed by California Public Utilities Commission ( CPUC) and existing technology questionnaires. I am the only statistician who are familiar with models in statistics and economics, I also served as a consultant to help colleague to understand the use of model (like linear regression, JEDI and Risk Premium) and explain model output. 

## K-Means Clustering
Now, we are planning estimate economic benefits of our investment condition on themes of the project. Since we have more than 100 detailed categories, we want to create more general categories by clustering based on the characters of the project.
I Initialized 8 categories first like Energy Efficient and Response Demand and get the center of the class. Then, we assign each xi to the cluster with the nearest center, where the distance between xi and cluster k is  with μj being the center of cluster k. Next, I recalculated the center μj of each cluster to be the centroid of its members. I repeated until convergence (e.g. no change in cluster membership).  

## KNN
For new project, I used KNN method to classify. In pattern recognition, the k-nearest neighbors algorithm (KNN) is a non-parametric method used for classification. The input consists of the k closest training examples in the feature space. The output is a class membership. An object is classified by a majority vote of its neighbors, with the object being assigned to the class most common among its k nearest neighbors.
I used cross-validation(with 5 folds) to find the best K and,  for each time, I used 80% of our projects information as training data to build the KNN model. I used the rest 20% data as test set to calculate the error rate based on the confusion matrix. I used the K that could give us the lowest error rate. For a new project, I calculated the distance between the new one and the old ones. Then, I selected the five nearest neighbor and label the new project based on these neighbors. 

## JEDI Model
I quantified the benefits mainly use JEDI model. The Jobs and Economic Development Impact (JEDI) model is a tool that estimate the economic impacts of constructing and operating power plants, fuel production facilities, and other projects at the local (usually state) level. JEDI results are intended to be estimates, not precise predictions.
I implemented this input-output model in VBA. Based on user-entered project-specific data or default inputs (derived from industry norms), JEDI estimates the number of jobs and economic impacts to a local area that can reasonably be supported by a power plant, fuel production facility, or other projects. The outputs of the model are jobs, earnings, and output are distributed across three categories:
•	Project Development and Onsite Labor Impacts
•	Local Revenue and Supply Chain Impacts
•	Induced Impacts

## Stress test
In order to estimate benefits of our investment under different scenarios, I conducted stress test. Stress test is an analysis or simulation designed to determine the ability of a given financial instrument or financial institution to deal with an economic crisis usually.  We set the stress based on decreasing market permeation and demand response and estimate how the benefits will change in different conditions. Besides, we needed to know what kind of stress will influence the return of our investments most. In addition, we calculated the threshold for the changing rate of market permeation and demand response under which the benefits of the project will not change.

## Decision Tree Model
A decision tree is a flowchart-like structure in which each internal node represents a "test" on an attribute each branch represents the outcome of the test, and each leaf node represents a class label (decision taken after computing all attributes). The paths from root to leaf represent classification rules.
In CEC, before we decide whether we should approve a project or not. We not only calculate the point estimate of the benefits of the project. We also test under different conditions to compare similar projects applications. We calculate potential benefits of each project based on certain conditions so we can determine which is the best under that condition. 

## Summary
Overall, I am satisfied with the internship in CEC. I am exposed to the whole process of data analysis, collection, cleaning, testing, modeling, visualizing and presenting results to tech/non-tech people to tell them the result. Thus, I am more experienced in using statistical tools and methodologies to deal with the real data and real word problem. Besides, I am more comfortable when dealing and prioritizing multiple tasks at same time. 



