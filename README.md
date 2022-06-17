# Fraud-Detection
Using Basic Neural Network to detect fraudulent transactions

**### Summary of actions taken**

**Location Data**

Using geopandas, I was able to calculate the distance between the merchant's cordinates and the cordinates of the location where fraud action happend,This was used to creat the distance colum while the logitute and latitude data was dropped from the dat frame

**Time Data**

Using sktime package, I calculated the Age of the customer from subtracting the date of birth from the transaction date. the date column was then dropped from the data frame.

**Dropping Columns**

Due to challenges with mermory, google coolab was unable to successfully execute the get dummies for our data frame. Hence most categorical features were dropped from the data frame, leaving only the ordinal categorical  features and the numerical features to work with.

**Data balance/imbalance**

The data was imbalanced and this was catered for by feeding the model with a bais at initialization. The bais value was set to be the log of the value positive outcomes divided by the negative outcomes

**Model Structure**

Due to restrictions on mermory allocation on google colab, model was kept moderate. "100 dense layers". Model achieved a vidation accuracy of 0.99

**Optimization Steps**

optimization of the model was done as well. With optimizer set to Adam, Drop out set to 0.5 and batch number and epoch set to 64 and 10 respectively
