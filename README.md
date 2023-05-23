# AirBNB
![](images/vacationhome.jfif)  
## Introduction
In this analysis, three questions were explored using AirBNB data from Seattle.
The three questions are described below.

## Question 1: Can I accurately predict price using just neighborhood location and size (max accommodation)?
### Methodology:
I first needed to determine if I needed to deal with any null values. There were none so I moved onto encoding categorical variables. I also needed to change the price column from a string to a float. I used regex and the to_numeric function to change the variable type. Lastly, I developed a model to predict price using a sk-learn's Linear Regression package. I chose this algorithm because I'm predicting for a numeric variable, and I'm attempting to determine if there is a relationship between the explanatory variables and the dependent variable.

### Results:
The resulting r-squared value for the model was 0.566 which means that there is evidence of a correlation between neighborhood location and size to price. As expected, a neighborhood's location and the size of the location are factors that contribue to an Airbnb's price. However, there was not enough evidence to support that price can be directly predicted using just these two variables.

## Question 2: Is there a relationship between review score rating and annual availability?
### Methodology:
When searching for null values, I saw that around 14.5% of records contained a null review score rating. I dropped these rows as this was the variable I was trying to predict. Encoding of categorical variables was not necessary for this experiment. For the model, I again used the Linear Regression package from sk-learn due to the same reasons for the 1st question. I'm predicting for a numeric variable and lookng for a relationship between the two variables.

### Results:
The resulting r-squared value for the model was -0.0005 which indicates that there is a near zero predictive ability for review score rating when looking at just annual availability.

### Question 3: Can the data be used to predict review scores? If so, what variables are the greatest contributors to a high review score?
### Methodology: 
For this question, a wide range of variables were considered to determine which ones had the greatest predictive power for review score rating. The variables that were considered are host response time, host response rate, superhost status, neighborhood group, property type, # of bathrooms, # of beds, and price. When looking for null values, it was observed that five of the variables contained null values. For review scores, the null values were simply dropped since this is the variable we are looking to predict. For response time, null values were replaced with another category which is "no time given". This was done in order to incorporate missing response times into the model development. For response rate, the null values were imputed with the mean as the vast majority of airbnb's had a 100% response rate. For # of bathrooms, the null values were imputed with 1 which was the median. Lastly, the price variable was changed from a string to a float. When encoding categorical variables, I saw that there were quite a few obscure property types that had very few numbers. Therefore, I condensed the number of variables by combining a few of the categorires into the "Others" variable. Afterwards, I created dummy variables for all categorical variables. For model development, I decided to use a random forest regression model due to the large number of explanatory variables as well as a relatively low number of records. The r squared score for the model was 0.29 which indicates a weak relationship between the explanatory variables and review score. However, when looking at feature importance, it appeared that price and host response rate had significantly greater influence on the review score than other variables. However, I concluded that it isn't possible to predict review score using variables such as host response time, price, neighborhood, etc.
