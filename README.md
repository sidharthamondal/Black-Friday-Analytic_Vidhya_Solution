# Black-Friday-Analytic_Vidhya_Solution# Black-Friday-Analytic_Vidhya_Solution
This is the solution for Analytics Vidhya Black Friday Solution .
As this is a retail based dataset and some 8 lakhs data point , 
the problem was to predict the purchase value of any  customer according to thier previous buying 
patterns or any new customer 

EDA:
Started with label encoding and other methods which you will find in my code file ,
Then went for correlation test as thier were no significant correlation with the dependent hence created 3 new features 
Bvalue , Pvalue , Pmax

Pvalue: I tried to estimate the price of a particular product by imputing the mean of the price for every unique product ID , as
I am working with both Train and Test stacked together and hence I have imputed the price of unique product ID by the mean of the 
whole purchase value .

BPower : I found that the unique ID columns have categorical varibales and hence is quite repitative in nature , so I 
created a feature which will procide the mean purchase value of each unique id 

Pmax :Here we are Adding another feature which will count the number of times that product have been bought 
at price above its actual mean value the process is same as that of previous loops
After adding this features I also thought of building some features where we can segment males and females but one could try this 
out from my code 

Modelling :
Did XGboost with finely tuned parameters 
