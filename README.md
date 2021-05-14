# Recipe Popularity Predictor
This is the final project for Ironhack Data Analytics Bootcamp, by Alexandre Sommerkamp

**Important Note: This repository is a work in progress.**

# Introduction
We will work on a recipe database from Food.com where users submitted recipes, and received ratings and comments from other users. We will try to quantify the recipe difficulty and try to predict user interaction with the recipe posted.  
## Background
This project is to be submitted to Ironhack as proof of the student capability to execute a project from beginning to end. We are given a full week to execute the project to try to corroborate our hypothesis. In this case I believe user interaction with recipes uploaded can be predicted by training a machine learning model with data regarding the recipe, the complexity of it, and the history of uploads from the user who posted. 

## Objectives
Decoding the database using Pickle, to have usable data to train the model

# Conclusions
None for now, work in progress

# Methodology


## Data source
The data has been published on Kaggle by a user called Shuyang Li. The original purpose of the dataset was to generate personalized recipes based on historical user preferences. The dataset includes 180K+ recipes and 700K+ recipe reviews of user interactions and uploads in Food.com from Jan 2000 to Dec 2018.

From the dataset it has been excluded originally recipes with less than 3 steps, and recipes with more than 20 ingredients, as well as users that have less than 4 reviews. 

You can download the data from this link: [Food.com Recipes and Interactions](https://www.kaggle.com/shuyangli94/food-com-recipes-and-user-interactions)

## Stack 
We will use Python for data wrangling and to apply the machine learning model.
Exploratory data analysis will be done with Python and Tableau, and the database will be built with MySQL 


## MVP
The minimum viable product to deliver will be a machine learning model trained to predict the number of comments the recipe will get from other users, together with a proper exploratory data analysis of the data, and Tableau Visualizations. 

## Extra Steps





