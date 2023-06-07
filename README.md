# Wine_Quality_Prediction
For this project, I used Kaggle’s Red Wine Quality dataset to build various classification models to predict whether a particular red wine is “good quality” or not. Each wine in this dataset is given a “quality” score between 0 and 10. For the purpose of this project, I converted the output to a binary output where each wine is either “good quality” (a score of 7 or higher) or not (a score below 7). The quality of a wine is determined by 11 input variables:

1.Fixed acidity
2.Volatile acidity
3.Citric acid
4.Residual sugar
5.Chlorides
6.Free sulfur dioxide
7.Total sulfur dioxide
8.Density
9.pH
10.Sulfates
11.Alcohol
12.Objectives

**The objectives of this project are as follows**

To experiment with different classification methods to see which yields the highest accuracy
To determine which features are the most indicative of a good quality wine

**Importing libraries**
First, I imported all of the relevant libraries that I’ll be using as well as the data itself.
**Understanding Data**
There are a total of 1599 rows and 12 columns. The data looks very clean by looking at the first five rows, but I still wanted to make sure that there were no missing values.
Next I wanted to see the correlations between the variables that I’m working with. This allows me to get a much better understanding of the relationships between my variables in a quick glimpse.
**Correlation Matrix**
Immediately, I can see that there are some variables that are strongly correlated to quality. It’s likely that these variables are also the most important features in our machine learning model, but we’ll take a look at that later.

**Convert to a Classification Problem**
Going back to my objective, I wanted to compare the effectiveness of different classification techniques, so I needed to change the output variable to a binary output.

For this problem, I defined a bottle of wine as ‘good quality’ if it had a quality score of 7 or higher, and if it had a score of less than 7, it was deemed ‘bad quality’.

Once I converted the output variable to a binary output, I separated my feature variables (X) and the target variable (y) into separate dataframes.

**Spliting data**
Next I split the data into a training and test set so that I could cross-validate my models and determine their effectiveness.

**Model: Random Forest**
Random forests are an ensemble learning technique that builds off of decision trees. Random forests involve creating multiple decision trees using bootstrapped datasets of the original data and randomly selecting a subset of variables at each step of the decision tree. The model then selects the mode of all of the predictions of each decision tree. What’s the point of this? By relying on a “majority wins” model, it reduces the risk of error from an individual tree.

