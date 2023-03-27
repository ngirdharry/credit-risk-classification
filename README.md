# Credit Risk Analysis 

# Project Overview

The purpose of this analysis is to build a model that can identify the creditworthiness of borrowers using a dataset of historical lending activity from a peer-to-peer lending services company. The model will be trained on various features of the borrowers, such as their income, employment status, and credit history, to predict the likelihood of them defaulting on their loan. The ultimate goal is to develop a reliable model that can be used to inform lending decisions and reduce the risk of default, while still providing access to credit for deserving borrowers. This analysis will use various techniques to preprocess the data, explore the relationships between features and the target variable, select appropriate features, and evaluate the performance of the model using various metrics.

I have utilized two machine learning models to assess loan risk and classify loans as either healthy (low-risk (0)) or non-healthy (high-risk(1)), based on their loan status. Specifically, I have developed a logistic regression algorithm that predicts the probability of a loan being healthy or non-healthy, using the status data from the lending company. This approach allows for an efficient and accurate assessment of loan risk, enabling lenders to make informed decisions and reduce the likelihood of loan default.

# Requirements 

Python, scikit-learn. 

# Results 

# Model 1 

I have developed a logistic regression model using the entire dataset provided by the financial company, which generated a balanced accuracy score of 94% (Model 1). The classification report for this model demonstrates good overall performance. However, given the class imbalance between healthy loans (low-risk) and non-healthy loans (high-risk), the model may be biased towards accurately predicting loan status as healthy, but not as accurately for non-healthy loans. This is indicated by the fact that the model achieved 100% accuracy in predicting healthy loans, but only 87% accuracy in predicting non-healthy loans, as shown in the classification report.

<img width="450" alt="Model 1 " src="https://user-images.githubusercontent.com/115658965/228045018-0b71e964-de15-43d0-abc1-3de3200ac078.png">

The presented confusion matrix below reveals that among the 18,759 loans classified as "healthy", the model correctly identifies 18,679 as healthy, but incorrectly classifies 80. Additionally, of the 625 loans classified as "non-healthy", the model correctly predicts 558, but misclassifies 67.

<img width="394" alt="Screen Shot 2023-03-27 at 3 28 45 PM" src="https://user-images.githubusercontent.com/115658965/228047563-37c75833-3a78-42b0-9ddb-0af21bcae295.png">



# Model 2 

Model 2 (below), which incorporates OverSampled data, demonstrated superior performance compared to Model 1, with a balanced accuracy score of 99%. This improvement can be attributed to the balanced dataset that enables more accurate predictions. With the inclusion of additional non-healthy loan data in the training set, Model 2 has a greater ability to identify and learn from patterns in high-risk loans. Specifically, the recall value for non-healthy loans increased from 0.89 in Model 1 to a perfect score of 1.00 in the oversampled Model 2. This result indicates that the model is more robust and has a higher capacity to identify errors in the classification of non-healthy (high-risk) loans as healthy (low-risk). This is an important aspect of loan risk assessment, as it enables lenders to avoid providing loans to high-risk borrowers who are more likely to default, thus minimizing the risk of financial loss.

<img width="490" alt="Model 2 " src="https://user-images.githubusercontent.com/115658965/228048949-56e351d2-d112-486e-a6a6-9fe250549945.png">

The presented confusion matrix below reveals that among the 18,759 loans classified as "healthy", the model correctly identifies 18,668 of them but incorrectly classifies 91. Further, out of the 625 loans classified as "non-healthy", the model correctly predicts 623 of them and only misclassifies 2. 

<img width="1086" alt="Screen Shot 2023-03-27 at 3 39 14 PM" src="https://user-images.githubusercontent.com/115658965/228049235-07af3626-0e80-434d-80b2-2065ec99137a.png">

# Summary 

The ability of a lending company to accurately identify healthy and non-healthy loans, based on the client's portfolio, is critical to their business success. Failure to do so can result in poor risk assessment, leading to financial losses for the lending company. Model 2 outperformed Model 1, as it was based on a balanced dataset and achieved higher accuracy scores and recall rates. This indicates that the model is less likely to misclassify non-healthy loans as healthy, which is preferable for the lending company as it minimizes the risk of providing loans to high-risk borrowers who are more likely to default. The improved performance of Model 2 highlights the importance of data balance and accuracy in machine learning-based risk assessment, particularly in the lending industry where financial stability depends on accurate loan risk evaluation.

# Credits
The dataset included was generated by edX Boot Camps LLC in partnership with the University of Toronto School of Continuing Studies, and is intended for educational purposes only.
