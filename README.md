# Neural_Network_Charity_Analysis

###Overview of the Analysis
In this Analysis we were tasked with figuring out which charities were more likely to be successful or efficient at using donations/funds. We did this by using the csv file provided and used deep neural networks in order to predict which charities would be more likely to succeed with said funds.

###Results
I utilized the keras model with 2 hidden layers, each with 80 and 30 nodes respectively. This was able to classify 74% of the charities accurately after doing a train/test data test. Depending on the requirements from leadership, 74% could either be satisfactory or unsatisfactory but more the most part, it does a good job at predicting the successful charities to donate to. We had to remove the "EIN" & "NAME" Columns as those were irrelevant to the model. We also bucketted or trimmed down some of the data in the "CLASSIFICATION" & "APPLICATION_TYPE" columns since there were more than 10 features on each of those. This grouped anything the first 9 features as "Others". From there, we encoded the categorical data as well and had to merge those columns with the original dataframe. This allowed the model to be able to weigh in the categorical data that was not numerical to meet it's criteria. I tried to increase the model past a 75% accuracy rate by adding a 3rd hidden layer and bucketing the application & classification type differently. However, it was not able to get past 75%, another thing I could have tried was to use different activation functions in order to see if that had any effect on the accuracy as well.

#Summary
The optimization was not successful at bringing the accuracy higher but a random forest model or a SVM would be able to at least match the accuracy of the deep neural network model and use a lot less code. I would recommend using different activation functions to get different results or get more data to analyze as the 3rd hidden layers and extra nodes were to no avail. 
