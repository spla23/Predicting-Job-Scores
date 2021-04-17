# Predicting-Job-Scores

Link to Google Doc:
https://docs.google.com/document/d/1c8UJi1vtScYgdSjItT6DPCU79tL5xgR38WEyfjxvQ_k/edit?usp=sharing

Link to Presentation: https://docs.google.com/presentation/d/11WXbeB7O-wPGv7oilwvdsQwW9ZAWiagmSIx41Ydi6-0/edit?usp=sharing

# Predicting Employee Perceptions of Data Science and Related Jobs from Glassdoor Reviews


### Team Members

Melanie

Youssef

Suha


### Link to Github Repo: [https://github.com/spla23/Predicting-Job-Scores](https://github.com/spla23/Predicting-Job-Scores)


### Link to Project Info:  [https://utoronto.bootcampcontent.com/utoronto-bootcamp/utor-tor-fin-pt-11-2020-u-c/-/tree/master/Projects/Project-02](https://utoronto.bootcampcontent.com/utoronto-bootcamp/utor-tor-fin-pt-11-2020-u-c/-/tree/master/Projects/Project-02)


### Link to Presentation:

[https://docs.google.com/presentation/d/11WXbeB7O-wPGv7oilwvdsQwW9ZAWiagmSIx41Ydi6-0/edit#slide=id.p](https://docs.google.com/presentation/d/11WXbeB7O-wPGv7oilwvdsQwW9ZAWiagmSIx41Ydi6-0/edit#slide=id.p)


### 


### To Do:



*   ~~Propose topic~~
*   ~~Find data~~
    *   ~~Company Data~~
    *   ~~Job Review Data~~
    *   ~~Job Description Data~~
*   ~~Load Data~~
    *   ~~Company Data~~
    *   ~~Job Review Data~~
    *   ~~Job Description Data~~
*   ~~Set Scope~~
    *   ~~Finalize Requirements and Tasks~~
        *   ~~Decide on questions to answer:~~
        *   ~~Assign tasks~~
*   ~~Data Prep~~

        ~~Spreadsheet with Column names and job titles:  https://docs.google.com/spreadsheets/d/1HyNPQ07ucuQ1zPYjoJN9KlSVbLb2fnT63-f6FUbJmXU/edit?usp=sharing~~

    *   ~~Drop irrelevant job titles~~
        *   ~~To keep: Data Analyst, Data Scientist, Data Engineer, Business Analyst, BI Analyst~~
    *   ~~Prepare tables that fulfill requirements (drop irrelevant columns)~~
    *   ~~Append, separate and join as necessary for model training~~
*   Data Exploration
    *   Model Training
    *   Model Evaluation
*   Hypotheses and Conclusions
*   Create a presentation

Possible Topics to test/analyze/predict scores for:

Youssef #1a Features of a company associated with good/bad job scores (from glassdoor.csv)



*   
Revenue


*   
Location


*   
Industry/Sector


*   
# of employees


*   
Pay range
Suha #1b Features of an employee/job associated with good/bad job scores (from glassdoor.csv)



*   Salary
*   Location
*   Industry/Sector
*   Turnover Rate (length of employment)
*   Percentile of pay range

Mel #2 Features of reviews associated with good/bad job scores (from glassdoor_reviews.csv)



*   NLP on reviews - what phrases and words are associated with what scores
*   Which features of reviews are associated with what job scores among data analyst related fields 

#3 Impact on overall job score by subcategory scores



*   
Benefits (structured and unstructured)


*   
Career Opportunity


*   
Work-Life Balance


*   
Senior Management


*   
Culture and Values

## 


## **Project Background**


#### Intro

Job reviews are a way for employees to give feedback on the quality of their job experience. Glassdoor.com is a popular career website that allows current and former employees to score their employer based on several criteria and leave a written review, highlighting pros and cons of the job. We want to explore models that can help predict job reviews on Glassdoor in the realm of data science and analysis and the features of jobs that lead to long-term satisfaction and reward for those in the domain of data.


#### Project Goal

The goal of this project is to predict quantitative star ratings (out of 5) of data science and related jobs at specific companies by applying sentiment analysis to job reviews and explore classification models to cluster other features of the data that demonstrate a relationship with higher and lower scores.


#### Problem & Hypothesis

What specific features of Data Science and related jobs are associated with high Glassdoor ratings? 

What features of companies employing Data and related jobs have a higher impact? 

Can we predict job ratings from a review and features of a company?


#### Hypotheses



*   There are features of companies that are associated with lower and higher satisfaction of employees.
*   There are sentiment features of job reviews that are associated with lower and higher satisfaction of data science and related employees.
*   There are sentiment features of job descriptions that are associated with lower and higher satisfaction of data science and related employees.


#### Use Cases



*   Help job seekers in data science identify the features of companies and roles that have the best prospects for long-term job satisfaction. 
*   Help job seekers in data scientists understand the words and phrases in job reviews most associated with long-term job satisfaction. 
*   Help job seekers in data science identify the words and phrases in job descriptions most associated with long-term job satisfaction. 


#### Assumptions



*   The specific words used in the job reviews matter to the learning model
*   The specific words used in the job descriptions matter to the learning model
*   The correlation of specific words used in the job descriptions and job reviews may matter to the learning model
*   The specific scores used by job reviewers are correlated with the sentiment of the job reviews
*   The specific scores used by job reviewers are NOT correlated with the sentiment of the job descriptions
*   The specific scores used by job reviewers are correlated with job satisfaction
*   Higher salaries (upper and lower bounds of salary) are correlated with higher job satisfaction
*   Longer tenure (upper and lower bounds of length of employment) is correlated with higher job satisfaction
*   The salary, length of employment, city of employment, job title and company **may **matter to the model
*   Older reviews are less predictive than more recent reviews



**Project Approach**


### Data

Data Sources


    Data:  



*   Using unstructured data (job reviews and job descriptions) for sentiment analysis
*   Using structured data (job scores, job attributes and company attributes) for classification and evaluation metric (accuracy of job score predictions)
*   Comprehensive:  https://www.kaggle.com/andresionek/data-jobs-listings-glassdoor?select=glassdoor_reviews.csv

    Job descriptions, company job score and company features sources:


        Job Listings from Glassdoor - includes unstructured data (job description) and  structured data (company score and company attributes) 


        ‘Data Scientist’ job listings from Glassdoor: [https://github.com/spla23/test_glassdoor](https://github.com/spla23/test_glassdoor)


        To Do:

*   get more titles (‘Data Analyst’, ‘Data Engineer’, ‘Business Analyst’)
*   [https://www.kaggle.com/andrewmvd/data-analyst-jobs](https://www.kaggle.com/andrewmvd/data-analyst-jobs)
*   [https://www.kaggle.com/andrewmvd/data-scientist-jobs](https://www.kaggle.com/andrewmvd/data-scientist-jobs)
*   [https://www.kaggle.com/andrewmvd/data-engineer-jobs](https://www.kaggle.com/andrewmvd/data-engineer-jobs)
*   [https://www.kaggle.com/andrewmvd/business-analyst-jobs](https://www.kaggle.com/andrewmvd/business-analyst-jobs)
*   [https://www.kaggle.com/josephgutstadt/data-jobs](https://www.kaggle.com/josephgutstadt/data-jobs)

    Company job score and Company features:


        Company (employer) data via API - includes structured data (company job score and company attributes) [https://www.glassdoor.ca/developer/companiesApiActions.htm](https://www.glassdoor.ca/developer/companiesApiActions.htm)


        To Do: 

*   get csv of API data

    Job reviews, company job score and job features sources:


        Scrape of Glassdoor with overall company score and subscores, review, title, length of employment. After doing all of this, we have a clean table with these columns: 'Summary','Date', 'OverallRating', 'WorkLifeBalance', 'CultureValues', 'CareerOpportunities', 'CompBenefits', 'SeniorManagement', 'Pros', 'Cons', ‘ProFeatures’, ‘ConFeatures’, ‘Sentiment score’, 'OverallRating to Sentiment Ratio'


        To Do: 

*   Run script
*   Get csv


#### Data Pre-Processing


#### Frameworks/Libraries used


#### Models to Explore

MLMs (1 that hasn’t been covered): NLP (Sentiment analysis of job reviews and descriptions - unstructured), Classification (K-Means or other to cluster features from sentiment and metadata), logistic regression and statistical tests can be used to select those features that have the strongest relationship with job scores in EDA phase


### Exploratory Data Analysis


#### Evaluation Metric

Prediction quality of Company job scores on these six dimensions from structured and unstructured criteria: 'OverallRating', 'WorkLifeBalance', 'CultureValues', 'CareerOpportunities', 'CompBenefits', 'SeniorManagement'

Analysis of the features of job reviews and job descriptions associated with a high level of job satisfaction (from employee scores out of 5 on 6 dimensions) and lifetime value of job (average annual salary x’s tenure in years) from Glassdoor reviews of Data Science and related jobs (Data Analyst, Data Engineer, etc.)


#### Exploration Results


##### 		Accuracy


##### 		Errors

		


### Summary and Conclusions


#### 
    Challenges


#### 
    Future Work


# 


# **Predict Ratings from NLP of review text**

Hypothesis: Review ratings can be predicted from review text.

Review Rating Prediction based on Review Text Content analysis

Preprocessing

Reduce columns to review text, review rating (and uuid of review)

Delete duplicate, null and NanN rows

Remove reviews from non-English speaking countries

Create text processor to extract meaningful words from text

	After applying, text should have

		No punctuation

		All lowercase

		Removed stopwords

		Removed additional stopwords

EDA

Value counts by rating

Models

first perform a TF-IDF term weighting and vectorizing

TF-IDF will process the text using “text_process” function 


    then convert the processed text to a count vector


    then assign a higher weight to words of more importance

Then run the classification algorithm


# 


# **Technical Requirements**

The technical requirements for Project 2 are as follows.



*   Create a Jupyter Notebook, Google Colab Notebook, or Amazon SageMaker Notebook to prepare a training and testing dataset. \

*   Optionally, apply a dimensionality reduction technique to reduce the input features, or perform feature engineering to generate new features to train the model. \

*   Create one or more machine learning models. \

*   Fit the model(s) to the training data. \

*   Evaluate the trained model(s) using testing data. Include any calculations, metrics, or visualizations needed to evaluate the performance. \

*   Show the predictions using a sample of new data. Compare the predictions if more than one model is used. \

*   Save PNG images of your visualizations to distribute to the class and instructional team and for inclusion in your presentation and your repo's README.md file. \

*   Use one new machine learning library, machine learning model, or evaluation metric that hasn't been covered in class. \

*   Create a README.md in your repo with a write-up summarizing your project. Be sure to include any usage instructions to set up and use the model.
