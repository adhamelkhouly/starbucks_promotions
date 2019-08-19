# starbucks_promotions
### Table of Contents
1. [Problem Statement](#prob)
2. [Project Description](#Project)
2. [Installation](#installation)
3. [File Description](#files)
4. [Results](#Results)
5. [Conclusions](#concs)
6. [Licensing, Authors, and Acknowledgements](#licensing)

## Problem Statements and Metrics <a name="prob"></a>
A. What are the different demographics of the Starbucks rewards program?
  - This is answered by creating multiple visualizations using the data provided.
    
B. What are the driving forces of the customer expenditure?
  - This is answered by building a linear regression model, with the total amount spent by each customer as the target value.
    
C. What is it that makes an offer effective?
  - The metrics used to answer this question is the viewership and completion records of a certain offer by certain demographics. A boolean metric was created (offer_effective) which has a value of 1 when an offer is, both, viewed and completed by a customer. An RFC model is created to classify that target value.

## Project Description <a name="Project"></a>
This project uses data obtained from [Starbucks](https://www.starbucks.com/). There are 3 data sets provided by Starbucks for the analysis. Namely: 
 - a portfolio.json file, which includes data about the offers themselves, their types and difficulty.
 - a profile.json file, which includes demographic information about the customers.
 - a transcript.json file, which includes customer activity

The starbucks data is analyzed to build a predictive classification model that attempts to predict
whether an offer is effective or not.  Effective offers are ones that are viewed and completed.

Exploratory data analysis is also made to understand the customer demographic more. Also, Customer expenditure features are explored.

The project is made up of 4 sections:
 1. EDA: data wrangling and analysis section pretaining to understanding the contents of the dataset. 
 2. Regression Model: built in an attempt to explore customer expenditure
 3. Classification Model: built in an attempt to predict effective offers
 4. Conclusions: this section discusses the findings of the project


## Installation and Running<a name="installation"></a>
- The requirements can be found in the [requirements.txt](requirements.txt) file.

- That file allows you to pip install all the necessary dependencies by running:
    `pip install -r requirements.txt` in your shell.
    
- Clone this project by using `git clone`

- Libraries:
   ```
   certifi==2019.6.16
   cycler==0.10.0
   joblib==0.13.2
   kiwisolver==1.1.0
   matplotlib==3.1.1
   numpy==1.17.0
   pandas==0.25.0
   progressbar==2.5
   pyparsing==2.4.2
   python-dateutil==2.8.0
   pytz==2019.2
   scikit-learn==0.21.3
   scipy==1.3.1
   six==1.12.0
   wincertstore==0.2
   ```

## File Descriptions <a name="files"></a>
```
│
├───data/
│       portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
│       profile.json - demographic data for each customer
│       transcript.json - records for transactions, offers received, offers viewed, and offers completed
│
├───plots - contains plots used in blog post
│
├───starbucks_offers.ipynb - jupyter notebook containing all the code
```

## Results <a name="Results"></a>
 1. The results of the EDA part of this project are encapsulated in multiple visualizations
 2. There is a Linear Regression model that is used to perform a simple analysis based on transaction amount. Answering the question:
 What are the main driving factors of customer expenditure?
 3. A Linear (Logistic Regression Model) and a Naive Classifier to serve as baseline classification model to compare RFC against
 4. A fine tuned RFC model with an f1-score of 0.79 and a classification error rate of less than 25%
 
## Conclusions <a name="concs"></a>
A. What are the different demographics of the Starbucks rewards program? Through EDA, I arrived at the following:
   - Customers enrolled in the rewards program are mostly in the 50-59 age group. However, that can be linked to their income being     higher than the previous age group
   - Viewed offers tend to be completed more often than offers that were not viewed by customers
   - There is no apparent relation between the reward and difficulty of a certain offer
   - There is no apparent relation between the reward and duration of a certain offer
   - Received offer were distributed evenly. Therefore, the sent amount of an offer was not a biasing factor

   
B. What are the driving forces of the customer expenditure? Using the Linear Regression model, I arrived at the following:
   - Female Customers tend to spend more than the rest of the customers
   - Discount offers lead to more customer expenditure
   - Genders of Male and Other were negative indicators to expenditure
   - Customers enrolled prior to 2018 are more likely to spend more

C. What is it that makes an offer effective? Through RFC,
   The most important features for that model were the following:
   1. Difficulty
   2. Duration
   3. Reward
## Licensing, Authors, Acknowledgements<a name="licensing"></a>
Credit to the Udacity lectures for some of the coding and visualization ideas, as well as Starbucks for providing the datasets.
