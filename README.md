# Amazon Review Sentiment Analysis


**The Note is uploaded under the name *'Sentiment Analysis.ipynb'***

**Code used to extract 20000 data sets from larget review set is under the name *Clothing_20000.ipynb***


## Review data analysis and sentiment prediction

- Here we are using the data from the amazon reviews,downloaded from http://jmcauley.ucsd.edu/data/amazon/ This site is having data from 1996 - 2014*
- The file we are using as dataset is json type file. We have reviewerID, asin, reviewerName, overall, summary columns in data.
- We have used clothing data from the mentioned website, initially using clothing_small.csv - having 1000 rows and if data doesnt give us expected resuts we used *clothing_20000.csv* set which has 20000 rows.

**Main logic in this code is that if the reviews in amazon are greater than or equal to 3 it is assumed as a postive review and machine is trained to pursue the same, any review less than 3 is assumed as a negative review**

*steps followed for the classification:*

## Data Loading
- Classifiers defining, which will be used in the code.
- Data loading from json file, loading strings to arrays.

## Feature Engineering
- Splitting data into train and test data using sklearn
- The data which we obtain will be in strings, they need to be vectorised, thus we vectorise the review data.

## Data Modelling
- After the initial data modelling has been done now trained the model using four classifying algos as follows:

  a. Support Vector Machine - Kernel = 'linear'
  b. Decision Tree
  c. K - Nearest Neighbours
  d. Logistic Regressor Classification

## Model improvement
The data i.e *Clothing_small.json* has generated a very low f1scores hence, I decided to re-model the data using bigger data having 20000 reviews set - *Clothing_20000.json* 

## Data Evaluation
- Verified the model using r2 and f1 scores and with few examples

***Logistic classification-***
- *f1-score -: Postive - 0.89; Negative - 0.49*
- *R2 score = 0.824*

***Linear support vector classification-***
- *f1-score -: Postive - 0.89; Negative - 0.48*
- *R2 score = 0.823*

