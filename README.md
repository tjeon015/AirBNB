# AirBNB
![](images/vacationhome.jfif)  
## Introduction
In this analysis, three questions were explored using AirBNB data from Seattle.
The three questions are described below.

## Question 1: Can I accurately predict price using just neighborhood location and size (max accommodation)?
### Methodology:
I first needed to determine if I needed to deal with any null values. There were none so I moved onto encoding categorical variables. I also needed to change the price column from a string to a float. I used regex and the to_numeric function to change the variable type. Lastly, I developed a model to predict price using a sk-learn's Linear Regression package. The resulting r-squared value for the model was 0.566 which means that there is evidence of a correlation between neighborhood location and size to price. However, there was not enough evidence to support that price can be directly predicted using just these two variables.

## Question 2: Is there a relationship between review score rating and annual availability?


### Question 3: Can the data be used to predict review scores? If so, what variables are the greatest contributors to a high review score?

