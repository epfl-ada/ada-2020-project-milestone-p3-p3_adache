# Predicting stock markets with Google Trends

## Abstract
<!--- A 150-word description of the project idea, goals, datasets used. What's the motivation behind your project? How do you propose to extend the analysis from the paper? What story would you like to tell, and why? --->

Predicting stock markets is hard due to its artificial nature and also because stock markets are influenced by economic news. As in the original paper, we want to evaluate the usage of Google Trends to better predict the present values of stock markets. The original paper explains the advantage of using Google Trends and introduces its readers to its subtilities. Only a few Google Trends data are included in the models and we would like to see if having more Google Trends can help to predict financial markets. We will use various Google Trends search subjects and evaluate which ones are the best to use. We also what to look at combinations of Google Trends search subjects and not only individual subjects. Our final goal is to be able to make predictions on the financial stocks and see which are the most relevant Google terms for predicting the stock markets.

## Research question
<!---A list of research questions you would like to address during the project. --->
1. Can we improve prediction of present stock markets with Google Trends?
2. What are the best Google Trends explaining variations in stock markets?
3. Is it usefull to combine several Google Trends subject?

<!--- -Which models should we explore?
  - Optimize baseline ARIMA model
  - Look at other models
- Which set of Google Trends key-words should we select
- How to perform feature selection to keep the most interesting Google Trends in our model --->


## Proposed dataset
<!---List the dataset(s) you want to use, and some ideas on how you expect to get, manage, process, and enrich it/them. Show us that you've read the docs and some examples and that you have a clear idea of what to expect. Discuss data size and format if relevant. It is your responsibility to check that what you propose is feasible given the datasets at hand. --->
- Yahoo historical service Data can give us the financial market data we are looking for. We thought of using two datasets:
  - [S&P500](https://query1.finance.yahoo.com/v7/finance/download/%5EGSPC?period1=1513728000&period2=1584780625&interval=1d&events=history) financial market from end 2017 to March 2020
  - [S&P500](https://query1.finance.yahoo.com/v7/finance/download/%5EGSPC?period1=1513728000&period2=1606159501&interval=1d&events=history) financial market from end 2017 to 2020. Extending the first one with the exceptional Covid-19 period which might be harder to predict.<br>
Note: we will use the adjusted closing value for the stock markets in the dataset.
- We will also need to get the [Google Trends](https://trends.google.com/trends/?geo=US) data from the website for each search term we want to investigate.

## Methods
**Data collection:** we will need to merge the dataset from the financial market and the google trends we decided to explore. The merging requires a little bit of attention because there aren't stock values for each day in the period due to the closing of stock markets at the weekend. We just have to make sure to properly handle this.<br>
**Finding the search terms:** We can make usage of previous work on the subject where some Google research terms were proposed [Google Trends keywords research inspiration](https://www.nature.com/articles/srep01684) and also bring some ideas that we might have. Especially considering the second dataset with the covid-19 crisis, where some research terms might differ from a normal period. Since we are using the US financial market, we might also want to consider using Google Trends only from the US or Worldwide and evaluate the difference appearing.<br>
**Data analysis:**
We are interested in the improvement of prediction using Google Trends. Also, it is interesting to see which are the most relevant Google Trends topics. Based on this we can see which are the search terms that seem to be correlated with financial markets. (Are there obvious or unexpected terms?)<br>
Once we have obtain the best individual subjects, we will try combining them to see if we can improve predictions.

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
- Once we agree on the subjects we want to consider, Fatih will handle the download and the preparation of the dataset to start the analysis. --
- Once this is done and data is shared, Etienne and Jeanne will get starting with the analysis.
- On week 2, we will divide the different research subjects so that everyone can perform some analysis on the assigned subjects.
- On week 3, Jeanne will focus on writing the data story and have some nice visualization to illustrate the finding.
- On week 3, Etienne will focus on preparing the short video while Fatih writes the report. As the three of us might need some visualization for our tasks, we will probably work together to define the illustrations we want to use.




## Questions for TAs
<!---Add here any questions you have for us related to the proposed project. --->
Any doubts or suggestions?<br>
Do you think the covid period is interesting and how to handle it? Combine it with the normal period (2018 to now) or treat it separately (march 2020 - now)?<br>
We also considered finding better model than the ARIMA in the original paper, is this worth considering ? Or it is better to focus on only one improvement (as proposed applying to other dataset)?
