# Re-Fridgerate: The Recipe Recommender 🥘 🍛 🦐 🍒
Lucas Mata, July 2021

## Contents
1. The idea
2. Minimum Viable Product
3. Methodology
4. Challenges
5. Future Iterations

## 1. The idea

Have you ever opened your fridge and not known what to prepare? Re-Fridgerate is an app that will sort this problem. 
With the fridge of the future in mind as a final iteration (if that even exists!), I created a recommender in which the user enters the ingredients he has on his fridge and it returns a few recipes he/she could make with those ingredients.

## 2. Minimum Viable Product

The MVP should be able to:
+ Get three ingredients from the user
+ Check if there are recipes in our database that contain those ingredients
+ Return a few recipes with the best sentiment score


## 3. Methodology

First, I created a [Trello Board](https://trello.com/b/YjeBv569/final-project) to plan all the tasks and subtasks i would need to take care off.

The main idea was to use three different fundamental skills: Web Scraping, EDA, Cleaning & Wrangling and Sentiment Analysis

1. I Web Scraped allrecipes.com using BeautifulSoup. I first tested scraping just one page, and i was able to get the fields i wanted - Recipe Title, Category and Subcategory, Ingredients, Reviews and URL. After realising that there was a number in the url that if increased by one would jump into a new page with a new recipe, I thought i could scrape for multiple recipes by creating a loop. In order to do this, i would need to define a function first with all the individual parts i had used before to scrape the test page that also inserts the restults into a dataframe. This function would be called later on with a while loop. I was able to get data for 1045 recipes.

2. EDA, Cleaning & Wrangling:
+ Checking for nulls, data types, number of rows and columns
+ converting everything to lower
+ removing unnamed column
+ cleaning ingredients: converting to list, tokenizing, keeping only alpha values, removing reserved words
+ Exploring Category and Subcategory in a bit more detail

3. I performed Sentiment Analysis over the customer reviews, with the objective of storing this information in a new column of our dataframe so the recommender would return the best scoring recipes. First i performed sentiment analysis over reviews from one recipe only as a test. I then cleaned the reviews by removing punctuation signs, tokenized them using NLTK to then remove stopwords and finally performed the sentiment analysis.

## 4. Challenges

## 5. Future Iterations

If you want more details on the actual code, be sure to check my jupyter notebook saved in this repo!
In case you have any questions, please contact me on [linkedin](https://www.linkedin.com/in/lucas-mata-vidosa-a53002ab/).

Thanks for reading!

Lucas
