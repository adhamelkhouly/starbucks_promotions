# starbucks_promotions
Data Science Project that uses data provided by Starbucks on their customer demographics and offers


### Table of Contents
1. [Project Description](#Project)
2. [Installation](#installation)
3. [File Description](#files)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Project Description<a name="Project"></a>
This project uses data obtained from [Starbucks](https://www.starbucks.com/)

The starbucks data is analyzed to build a predictive classification model that attempts to predict
whether an offer is effective or not.

Effective offers are ones that are viewed and completed.

Exploratory data analysis is also made to understand the customer demographic more.

Customer expenditure features are also explored.

The project is made up of:
 - EDA: data wrangling and analysis section pretaining to understanding the contents of the dataset.
 - Regression Model: built in an attempt to explore customer expenditure
 - Classification Model: built in an attempt to predict effective offers
 - Conclusions: this section discusses the findings of the project


## Installation and Running<a name="installation"></a>
- The requirements can be found in the [requirements.txt](requirements.txt) file.

- That file allows you to pip install all the necessary dependencies by running:
    `pip install -r requirements.txt` in your shell.

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
## Licensing, Authors, Acknowledgements<a name="licensing"></a>
Credit to the Udacity lectures for some of the coding and visualization ideas, as well as Starbucks for providing the datasets.