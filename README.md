![banner](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/blob/main/images/vongole-banner.png?raw=true)

# Recipe Popularity Predictor
This is the final project for Ironhack Data Analytics Bootcamp, by Alexandre Sommerkamp

**Important Note: This repository is currently a work in progress.**

* [Introduction](#Introduction)  
* [Conclusions](#Conclusions)  
* [Methodology](#Methodology)  


* [Introduction](#Introduction)  
* [Conclusions](#Conclusions)  
* [Methodology](#Methodology)  


# Introduction
We will work on a recipe database from Food.com where users submitted recipes, and received ratings and comments from other users. We will try to quantify the recipe difficulty and try to predict user interaction with the recipe posted.  
## Background
This project is to be submitted to Ironhack as proof of the student capability to execute a project from beginning to end. We are given a full week to execute the project to try to corroborate our hypothesis. In this case I believe user interaction with recipes uploaded can be predicted by training a machine learning model with data regarding the recipe, the complexity of it, and the history of uploads from the user who posted. 

## Objectives
Decoding the database using Pickle, to have usable data to train the model

# Conclusions
None for now, work in progress

# Methodology
Things we want to learn about
- Using pickle to codify/decode the ingredient map 
- Using sklearn pipelines to apply several ML models easily, and create more readable notebooks
- Building a MySQL database to dump this data and be able to retrieve it easily for visualizations

## Steps:

- We made a first exploration of the data [INSERT LINK]
- Planned how the dataframe for training the model should look like [LINK TO NOTEBOOK]
- Started touching the interactions table. Bringing in the submission date of the recipe being commented, in order to analyse how the reaction of the users look like for different users. with this data we can also use 

#### Questions for Tableau we can try to answer:
How many people review their own recipes, with how much rating and sentiment (We could not analyze this. Most of contributor IDS don't match the user IDs that comment. this could be due to users having different ID numbers when posting and when commenting, or really because most people who post do not comment. 
how is the reaction of users, how late is the interaction distribution, do people react early? late? distributed through time?
INSERT GRAPH SNIP FROM TABLEAU 
Users comment recipes mostly the day after they are posted, then drop exponentially. There is a small surge of activity every year after the recipe was submitted. This could be due to the recipes being seasonal. People tend to cook more christmas recipes on christmas time, for example
find best contributors, we can do a RFM analysis of posting users, as if they were our users, how many interaction they generate, this translates to traffic in the page.
a highlight is that there is a stop of posting at around 2010, being the biggest contributor in that group. There is very high disparity between big posters and smaller posters. 
INSERT GRAPH SNIP FROM TABLEAU  
how many recipe postings we had over time and how many interactions also happened over time
We can see that activity dropped since 2010, and interestingly the complexity of recipes, or the amount of steps that are needed, as well as the average rating drops
INSERT GRAPH SNIP FROM TABLEAU



## 
Shaping the table we will use for training:
* Recipe ID: 
* User:
- no. of recipes submitted
- no. of comments per recipe (average)
- sentiment of the comments (average)
- rating (average)
* from the recipes:
- time to cook
- number of steps
- number of ingredients
- time since posted
- complexity (analysis of verbs in steps, scoring complexity)
- ingredient category (categorizing ingredients in meat/fish, dairy, vegetable)
- Nutritional value








## Data source
The data has been published on Kaggle by a user called Shuyang Li. The original purpose of the dataset was to generate personalized recipes based on historical user preferences. The dataset includes 180K+ recipes and 700K+ recipe reviews of user interactions and uploads in Food.com from Jan 2000 to Dec 2018.


You can download the data from this link: [Food.com Recipes and Interactions](https://www.kaggle.com/shuyangli94/food-com-recipes-and-user-interactions)

### Table description:
* RAW_interactions: 
-user_id and recipe_id: User and recipe it interacted with. 
-date: date of the interaction as YYYY-MM-DD
-rating: 
-interactions tables:  These were provided for the original purpose of this dataset, and include data regarding past interactions of users with the recipes posted. We will not be using this data for this project.



## Stack 
We will use Python for data wrangling and to apply the machine learning model.
Exploratory data analysis will be done with Python and Tableau, and the database will be built with MySQL 


## MVP
The minimum viable product to deliver will be a machine learning model trained to predict the number of comments the recipe will get from other users, together with a proper exploratory data analysis of the data, and Tableau Visualizations. 
We will first work with 2% of the dataset, due to the vast size of it, and then feed the model a bigger set. 


## Extra Steps





