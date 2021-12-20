# Outlier-Removal-PYSPARK
 This repository shows, how to identify and remove the outliers using Pyspark

1. The initial dataset contains 440 records with 8 features
1. There are total 6 numerical features & 2 categorical features
The original spark dataframe has the datatypes of strings
The numerical features were converted into IntegerType using cast function
Created a customized function to identify outliers in each record
Applyng the above customized function, enables us to identify total outliers in each record, based on each feature
Filtering the dataset based on the total outliers which are <=1, to eliminate the records with more than 2 outliers
The new dataframe, contains 399 records after removing the outliers against 440 records in the inital data frame
Comparing the outliers from the original dataset to the new dataset after outlier removal using a box plot
There are still some outliers available in the dataset., even after removing majority of the outliers.
This shows that the data is skewed, however, the majority of the outliers are removed
