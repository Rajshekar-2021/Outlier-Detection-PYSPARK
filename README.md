# Outlier-Removal-PYSPARK
 This repository shows, how to identify and remove the outliers using Pyspark
 
### The dataset is collected from https://archive.ics.uci.edu/ml/datasets/wholesale+customers

### Attribute Information:

1. FRESH: annual spending (m.u.) on fresh products (Continuous);
1. MILK: annual spending (m.u.) on milk products (Continuous);
1. GROCERY: annual spending (m.u.)on grocery products (Continuous);
1. FROZEN: annual spending (m.u.)on frozen products (Continuous)
1. DETERGENTS_PAPER: annual spending (m.u.) on detergents and paper products (Continuous)
1. DELICATESSEN: annual spending (m.u.)on and delicatessen products (Continuous);
1. CHANNEL: customersâ€™ Channel - Horeca (Hotel/Restaurant/CafÃ©) or Retail channel (Nominal)
1. REGION: customersâ€™ Region â€“ Lisnon, Oporto or Other (Nominal)

### REGION Frequency
1. Lisbon 77
1. Oporto 47
1. Other Region 316
#### Total 440

### CHANNEL Frequency
1. Horeca 298
1. Retail 142

#### Total 440

 
### Observations :

1. The initial dataset contains 440 records with 8 features
1. There are total 6 numerical features & 2 categorical features
1. The original spark dataframe has the datatypes of strings
1. The numerical features were converted into IntegerType using cast function
1. Created a customized function to identify outliers in each record
1. Applyng the above customized function, enables us to identify total outliers in each record, based on each feature
1. Filtering the dataset based on the total outliers which are <=1, to eliminate the records with more than 2 outliers
1. The new dataframe, contains 399 records after removing the outliers against 440 records in the inital data frame
1. Comparing the outliers from the original dataset to the new dataset after outlier removal using a box plot
1. There are still some outliers available in the dataset., even after removing majority of the outliers.
1. This shows that the data is skewed, however, the majority of the outliers are removed

![image](https://user-images.githubusercontent.com/90382338/146808253-8e088387-df8b-434f-89c6-af258174286a.png)

