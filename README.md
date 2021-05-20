![banner](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/blob/main/images/vongole-banner.png?raw=true)

# Recipe Popularity Predictor
This is the final project for Ironhack Data Analytics Bootcamp, by Alexandre Sommerkamp

**Important Note: This repository is currently a work in progress.**

* [Introduction](#Introduction)  
* [Conclusions](#Conclusions)  
* [Methodology](#Methodology) 
* [The Data](#Data-source) 
* [Check the Tableau dashboards](https://public.tableau.com/profile/alex2690#!/vizhome/AnalysisofFood_comrecipedatabaseanduserinteractions/AnalysisofFood_comrecipedatabase)

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

## Data source
The data has been published on Kaggle by a user called Shuyang Li. The original purpose of the dataset was to generate personalized recipes based on historical user preferences. Scraped from Food.com, and it consists of data from 2000 to 2018.

You can download the data from this link: [Food.com Recipes and Interactions](https://www.kaggle.com/shuyangli94/food-com-recipes-and-user-interactions)

### Table descriptions
* RAW_interactions.csv : Raw interaction data, over 1M lines and several featuers. 
* RAW_recipes.csv : Raw recipe data, with nutritional values, ingredients, steps, and many other features.
* ingr_map.pkl : codified table with pickle, which has data about ingredients, and simplified names that substitute current ones in the raw dataset.
* PP_recipes, PP_users and test, train, and validation sets: These are tokenized tables, as well as sets to train a machine learning model which purpose was to synthesise tailored recipes based on user previous activity in the site.  They are not used in this project.
**For more info about the data used refer to [0-import-discover-data.ipynb](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/blob/main/code/0-import-discover-data.ipynb)**

## Stack 
* With python: 
	- Pandas and numPy for wrangling.
	- Seaborn and MatPlotLib for visualizations.
	- Spacy and TextBlob for natural language processing
	- SciKitLearn for machine learning deployment
* Tableau to create Visualizations
* Slides.com for the [presentation](https://slides.com/alex-skp/predicting-user-interaction)

## In this repository:
* In the folder [code](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/tree/main/code) you can find the jupyter notebooks with the python code used to access the data, clean it, creating a data table to train our machine learning model, and the application of these models through data pipelines developed with the library sklearn. 
* A [tableau story](https://public.tableau.com/profile/alex2690#!/vizhome/AnalysisofFood_comrecipedatabaseanduserinteractions/AnalysisofFood_comrecipedatabase) with interactive dashboards to discover the data. You can check [my profile]https://public.tableau.com/profile/alex2690#!/?newProfile=&activeTab=0) for visualizations related to other projects. 

## Extra Steps
* Working more specifically in the machine models applied. The current status is a quick application in order to test the sklearn pipelines, so definitive conclusions can't be made from those results.
* Making a better Natural Language analysis of the text files, and pulling more information from the actual qualitative information in the dataset. 
* Creating a MySQL database in order to simplify the retrieval and manipulation of the data before feeding it to the machine learning models. 





