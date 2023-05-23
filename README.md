# AirBNB
![](images/vacationhome.jfif)  
## Introduction
In this analysis, three questions were explored using AirBNB data from Seattle.
The three questions are described below.

## Question 1: Can I accurately predict price using just neighborhood location and size (max accommodation)?
### Methodology:
I first needed to determine if I needed to deal with any null values. There were none so I moved onto encoding categorical variables. I also needed to change the price column from a string to a float. I used regex and the to_numeric function to change the variable type. Lastly, I developed a model to predict price using a sk-learn's Linear Regression package. I chose this algorithm because I'm predicting for a numeric variable, and I'm attempting to determine if there is a relationship between the explanatory variables and the dependent variable.

### Results:
The resulting r-squared value for the model was 0.566 which means that there is evidence of a correlation between neighborhood location and size to price. However, there was not enough evidence to support that price can be directly predicted using just these two variables.

## Question 2: Is there a relationship between review score rating and annual availability?
### Methodology:
When searching for null values, I saw that around 14.5% of records contained a null review score rating. I dropped these rows as this was the variable I was trying to predict. Encoding of categorical variables was not necessary for this experiment. For the model, I again used the Linear Regression package from sk-learn due to the same reasons for the 1st question. I'm predicting for a numeric variable and lookng for a relationship between the two variables.

### Results:


### Question 3: Can the data be used to predict review scores? If so, what variables are the greatest contributors to a high review score?

