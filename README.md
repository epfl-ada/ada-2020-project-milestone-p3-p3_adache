<!--- P3 info : (https://docs.google.com/document/d/1PHv1wcScfFz1zF9nuzbhlF89lH-I2x1d-QoUmJZrSFc/edit) --->

# Predicting the Stock Market using Google Trends

## Abstract
<!--- A 150-word description of the project idea, goals, datasets used. What's the motivation behind your project? How do you propose to extend the analysis from the paper? What story would you like to tell, and why? --->

Stock markets are hard to predict because they depend on a tremendous amount of factors including the historical data and the economic news. As in the original paper, we want to evaluate the use of Google Trends in nowcasting but in this different practical case of stock market.  
The original paper explains how Google Trends are helpful in improving forecasts with a baseline model. In contrast, we will explore different prediction models to choose the optimal one to forecast the price movement of one of the most popular US Stock index, the S&P 500. 
Then, Google Trends data will be introduced to improve these predictions. A Google Trends keywords selection will be performed beforehand to keep the most relevant ones for each study case.  At the end, we'll have the possibility to test our models in predicting the stock prices of a few big companies. Examples can include Microsoft, Amazon, and Apple. 


## Research questions
<!---A list of research questions you would like to address during the project. --->
1. What are the best models to predict the near term price movement of stock markets, more specifically the S&P500 index ?
2. Can we improve our predictions using Google Trends? If yes, to what extent ? 
3. Which Google Trends keywords are most relevant in explaining stock market price variations and why ?

<!--- -Which models should we explore?
  - Optimize baseline ARIMA model
  - Look at other models
- Which set of Google Trends key-words should we select
- How to perform feature selection to keep the most interesting Google Trends in our model --->


## Proposed dataset
<!---List the dataset(s) you want to use, and some ideas on how you expect to get, manage, process, and enrich it/them. Show us that you've read the docs and some examples and that you have a clear idea of what to expect. Discuss data size and format if relevant. It is your responsibility to check that what you propose is feasible given the datasets at hand. --->

[Yahoo Finance](https://finance.yahoo.com/lookup) Historical Data service can give us the financial market data we are looking for. We're planning to use the following dataset :
- [S&P500](https://query1.finance.yahoo.com/v7/finance/download/%5EGSPC?period1=1388534400&period2=1606435200&interval=1d&events=history&includeAdjustedClose=true) index, from the beginning of 2004 to today  
  
The following datasets will be possibly included for further analysis, all for the period of the beginning of 2004 to today : 
  - [Amazon](https://query1.finance.yahoo.com/v7/finance/download/AMZN?period1=1388534400&period2=1606435200&interval=1d&events=history&includeAdjustedClose=true) stock
  - [Microsoft](https://query1.finance.yahoo.com/v7/finance/download/MSFT?period1=1072915200&period2=1606435200&interval=1d&events=history&includeAdjustedClose=true) stock
  - [Apple](https://query1.finance.yahoo.com/v7/finance/download/AAPL?period1=1072915200&period2=1606435200&interval=1d&events=history&includeAdjustedClose=true) stock  
  
  Note: we will use the adjusted closing value for the stock markets in the dataset.

We will also need to get the [Google Trends](https://trends.google.com/trends/?geo=US) data from the website for each search term we want to investigate.

## Methods
**Data collection and wrangling:** We will need to merge the dataset from the financial market and the Google Trends we decided to explore. The merging requires all of our attention because there aren't stock values for each day in the period due to the closing of stock markets at the weekend. Moreover, Google provides daily, weekly or monthly datapoints for its Trends depending on the requested period. If there are any missing Trends values, we'll be able to reconstruct them through interpolation. Google Trends gives only absolute data points but we'll consider the *relative* changes in search volume using *n* time units of past data points, n to be defined.  <br>

**Finding the relevant search topics:** We can make use of a previous work on the subject where some Google research terms were proposed : [Quantifying Trading Behavior in Financial Markets Using Google Trends](https://www.nature.com/articles/srep01684).
We can also try to bring new keyword ideas that we might have. To illustrate this, we could use the keyword `iPhone` to improve the forecasting of the Apple stock. [Related Searches](https://support.google.com/trends/answer/4355000?hl=en#:~:text=When%20you%20search%20for%20a,the%20tab%20for%20your%20term.) tool integrated in Google Trends can be useful to this effect.  
Since we are assessing the US financial market, we might also want to consider using Google Trends  from the US or Worldwide and evaluate the difference appearing.<br>

**Model evaluation:** To make our predictions, we'll test and evaluate different parameters of an autoregressive model based on a moving window. Then, we'll try to improve these predictions using Google Trends data. In order to do so, we will explore different regression models including Linear Regression and Gradient Boosting Regression. 

**Data analysis:** We are interested in the improvement of prediction using Google Trends. Also, it is interesting to see which are the most relevant Google Trends topics. Based on this we can see which are the search terms that seem to be most correlated with financial markets. <br>
Once we have obtained the best individual search topics, we will try to combine them to see if we can improve the predictions.

## Proposed timeline
**Week 1:** Getting started with the new data (downloading, cleaning, and merging) and start the analysis <br>
**Week 2:** Apply the model to the new data and start the analysis of the best search terms, try the best combination of terms.<br>
**Week 3:** Finalize the analysis, preparing the data story, report, and short video.<br>

<!--- - December 1st: We have decided which Google Trends key-words we want to use in our model and have imported it. That is, which words are the most related to the finance market and are the most likely to bring information and have an impact on our model's prediction.
- December 5th: Google Trend data and Finance data are imported and cleaned. Our data is ready to be used.
- Research on different models. --->

## Organisation within the team
<!---A list of internal milestones up until project milestone P4. Add here a sketch of your planning for the next project milestone. --->
- On week 1, each member of the team will individually find good Google Trends search subject to consider. 
- Once we agree on the subjects we want to consider, Fatih will handle the download and the preparation of the dataset to start the analysis. 
- Once this is done and data is shared, Etienne and Jeanne will get starting with the analysis.
- On week 2, we will divide the different research subjects so that everyone can perform some analysis on the assigned subjects.
- On week 3, Jeanne will focus on writing the data story and have some nice visualization to illustrate the finding.
- On week 3, Etienne will focus on preparing the short video while Fatih writes the report. As the three of us might need some visualization for our tasks, we will probably work together to define the illustrations we want to use.




## Questions for TAs
<!---Add here any questions you have for us related to the proposed project. --->
Any doubts or suggestions?<br>
We're thinking of finding a better model than the ARIMA in the original paper, e.g. neural networks, is this worth considering ? 


