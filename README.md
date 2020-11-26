P3 info : (https://docs.google.com/document/d/1PHv1wcScfFz1zF9nuzbhlF89lH-I2x1d-QoUmJZrSFc/edit)

# Title 

## Abstract
A 150 word description of the project idea, goals, datasets used. What's the motivation behind your project? How do you propose to extend the analysis from the paper? What story would you like to tell, and why? 

In this project, we want the show the difference when making predictions with and without the use of Google Trends in the model. 
Although the paper explains the advantage of using Google Trends and introduce its readers to its subtilities, it still uses a baseline model to illustrate its point. First, we would like to look at other prediction models in order to choose the optimal one to make our predictions. Then, our model will by applied to a different set of data. Our final goal is to be able to make predictions on the financial stock analysis. 

## Research question
A list of research questions you would like to address during the project.

- Which models should we explore?
  - Optimize baseline ARIMA model
  - Look an other models
- Which set of Google Trends key-words should we select
- How to perform feature selection in order to keep the most interesting Google Trends in our model
-


## Proposed dataset
List the dataset(s) you want to use, and some ideas on how you expect to get, manage, process, and enrich it/them. Show us that you've read the docs and some examples, and that you have a clear idea on what to expect. Discuss data size and format if relevant. It is your responsibility to check that what you propose is feasible given the datasets at hand.
- Yahoo historical service Data, S&P500 financial market from end 2017 to march 2020: https://query1.finance.yahoo.com/v7/finance/download/%5EGSPC?period1=1513728000&period2=1584780625&interval=1d&events=history
- Same data until end of November to use Covid-19 period: https://query1.finance.yahoo.com/v7/finance/download/%5EGSPC?period1=1606159501&period2=1584780625&interval=1d&events=history
- Google Trends keywords research inspiration: https://www.nature.com/articles/srep01684


## Methods

## Proposed timeline

- December 1st: We have decided which Google Trends key-words we want to use in our model and have imported it. That is, which words are the most related to the finance market and are the most likely to bring information and have an impact on our model's prediction.
- December 5th: Google Trend data and Finance data is imported and cleaned. Our data is ready to be used.
- Research on different models.

## Organisation within team
A list of internal milestones up until project milestone P4. Add here a sketch of your planning for the next project milestone.
## Questions for TAs
Add here any questions you have for us related to the proposed project.
