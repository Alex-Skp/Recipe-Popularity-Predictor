![banner](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/blob/main/images/vongole-banner.png?raw=true)

# Recipe Popularity Predictor
This is the final project for Ironhack Data Analytics Bootcamp, by Alexandre Sommerkamp

* [Introduction](#Introduction-and-background)  
* [Conclusions](#Conclusions)  
* [Methodology](#Methodology) 
* [The Data](#Data-source) 
* [Check the Tableau dashboards](https://public.tableau.com/profile/alex2690#!/vizhome/AnalysisofFood_comrecipedatabaseanduserinteractions/AnalysisofFood_comrecipedatabase)

# Introduction and background
This project is to be submitted to Ironhack as proof of the student capability to execute a project from beginning to end. We are given a full week to execute the project to try to corroborate our hypothesis. In this case I believe user interaction with recipes uploaded can be predicted by training a machine learning model with data regarding the recipe, the complexity of it, and the history of uploads from the user who posted. 
For this a database from Food.com will be used, a web portal open from 2009 where recipes are posted and commented by users. 

## Objectives
1- Creating a machine learning model that predicts the number of comments a recipe will receive in the first 30 days, and the average rating of the recipe, by creating features and building a database to train several regression models.    
2- Making an exploration of the data with Tableau, answering specific [questions](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/tree/main/tableau-eda) and creating an [interactive dashboard](https://public.tableau.com/profile/alex2690#!/vizhome/AnalysisofFood_comrecipedatabaseanduserinteractions/AnalysisofFood_comrecipedatabase).
3- Exploring new tools for wrangling and deploying machine learning models, as this project is done for educational purposes. 

# Conclusions
- From the exploratory analysis we could see that food.com had great user interaction at two years since conception, and kept a fair amount of activity through the years, until 2010, where it plummeted.   
- We could see that users tend to rate recipes high when they post a review, and that this tendency drops as the days pass since the posting of the recipe, and it also becomes more unpredictable. This makes it hard for machine learning models to predict accurately the user interaction based on the parameters facilitated.  
- In this project we achieved the best result with a random forest regressor to predict the number of users, and with linear regression for the rating, however the results achieved with the models are not good enough, as their average error is bigger than the average user interaction, and for the rating, the average error of .5 points also is not good enough, as most recipes already fall between 4 and 5 points.   
- We succesfully deployed sklearn pipelines and were able to test several models in a very simple way, but more work is to be done in measuring the accuracy of the models, as well as tweaking the parameters of them.  

# Methodology

- Downloaded the data from [Kaggle](https://www.kaggle.com/shuyangli94/food-com-recipes-and-user-interactions) and made a first exploration of the data in [this notebook](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/blob/main/code/0-import-discover-data.ipynb)
- Planned the [features](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/blob/main/images/table-planning.JPG) that can be extracted from the data 
- Engineered the features that we would feed later to the machine learning model, you can see the process in [this notebook](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/blob/main/code/1-generating-features-and-wrangling.ipynb)
- During that process we could create a richer database to feed in Tableau, answer the [questions](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/tree/main/tableau-eda) que placed ourselves, and created this [dashboard](https://public.tableau.com/profile/alex2690#!/vizhome/AnalysisofFood_comrecipedatabaseanduserinteractions/AnalysisofFood_comrecipedatabase).
- We went on a deeper analysis of the features, and decided the steps we would need to preprocess our data. Deployed the pipelines and tried several models. The process can be found in [this notebook](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/blob/main/code/2-Applying-regression-models-with-pipelines.ipynb)
-Prepared a presentation to be delivered to the rest of the cohort, using using [slides.com](https://slides.com/alex-skp/predicting-user-interaction).

## Data source
The data has been published on Kaggle by a user called Shuyang Li. The original purpose of the dataset was to generate personalized recipes based on historical user preferences. Scraped from Food.com, and it consists of data from 2000 to 2018.

You can download the data from this link: [Food.com Recipes and Interactions](https://www.kaggle.com/shuyangli94/food-com-recipes-and-user-interactions)

**Table descriptions**
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





