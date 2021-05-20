![banner](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/blob/main/images/vongole-banner.png?raw=true)

# Tableau Exploration:


#### Questions for Tableau want to answer
In order to gain insight in the data, we will plot it with tableau, and we asked ourselves the following questions:

1- How many people review their own recipes, with how much rating and sentiment?  
We could not analyze this as most of contributor IDS don't match the user IDs that comment. this could be due to users having different ID numbers when posting and when commenting, or really because most people who post do not comment. 

2- How is the reaction of users, how late is the interaction distribution, do people react early? late? distributed through time?
Users comment recipes mostly the day after they are posted, then drop exponentially. There is a small surge of activity every year after the recipe was submitted. This could be due to the recipes being posted and searched for in a yearly season. 
![picturetableau](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/blob/main/images/inter-with-recipes.JPG?raw=true)

3- Which are the best recipe contributors? What is the health status of our page? 
For this we can do a RFM analysis of posting users, as if they were our customers, and analyze how many interaction they generate, as this translates to traffic in the page, and more advertising revenue.
One highlight is that there is a stop of posting at around 2010, which could be caused by the rise of Youtube, and the drifting of viewers going to video recipes from written instead. Our biggest contributor stopped posting around that time too. 
![picturetableau2](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/blob/main/images/RFM-contributors.JPG?raw=true) 

4- How many recipe postings we had over time and how many interactions also happened over time?
We can see that activity dropped since 2010. Towards the latest years recipes tended to be more complicated in the amount of steps needed, and user's recipe ratings dropped in average. 
![picturetableau3](https://github.com/Alex-Skp/Recipe-Popularity-Predictor-work-in-progress/blob/main/images/data-span.JPG?raw=true)

## Data source
The data has been published on Kaggle by a user called Shuyang Li. The original purpose of the dataset was to generate personalized recipes based on historical user preferences. Scraped from Food.com, and it consists of data from 2000 to 2018.

You can download the data from this link: [Food.com Recipes and Interactions](https://www.kaggle.com/shuyangli94/food-com-recipes-and-user-interactions)
