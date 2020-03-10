![](https://img.shields.io/badge/Anish-Approved-brightgreen.svg)

# WSB ML Project

## Anish Yakkala, Adrien Chaussabel, Lemar Popal

Download dataset from https://www.kaggle.com/theriley106/wallstreetbetscomments

### Week 1 (02/25/2020-03/02/2020)

- Get Data
  - Use `yfinance` library in Python to get historical finance data
  - Use https://github.com/theriley106/TheWSBIndex for dataset of WSB comments and list of company tickers
- Extract Tickers of WSB Comment Data
  - Use regex on `body` column of WSB comments dataset and explode list of tickers to get datasets for specific tickers
- Work on EDA for WSB Comment Data
  - Focusing on TSLA, and making code reproducible to do this with other tickers
  - Sell Mentions seem to fit nicely to Volume 
  ![TESLA](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/TESLA_sell_volume.png)
- Join historical financial data to the comment history
  - Join on `Date` Column.
- Leverage Sentiment Analysis Algorithm from https://github.com/theriley106/TheWSBIndex

- Possible ML idea
  - Based on past open and close prices, WSB comments, and today's open price for stocks predict the closing price. This will provide a good strategy whether to buy the stock and sell before after-hours.
  
### Week 2 (3/03/2020 - 3/10/2020)

- Expand on the Sentiment Analysis Alogrithm from https://github.com/theriley106/TheWSBIndex
- Looked at how upvote history fits with various features corresponding to financial movement
![score_vs_volume](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/volume_vs_score.png)
- Made a simple Exponential Moving Average Algorithm to fit onto our data
![moving_average](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/Exponential_Moving_Average.png)
NOTE: THESE RESULTS ARE DUE TO A MISTAKE IN OUR CODE (KEEPING IT IN BECAUSE IT SHOWS HOW GOOD BUT BAD OVERFITTING IS)
- Fit a LSTM model onto our dataset with the features derived from the Sentiment Analysis Algorithm. (Focused on TSLA)
![first_pass](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/first_attempt_lstm.png)
- Working on hypertuning the features for LSTM to reduce RMSE as much as we can
- Look at using the Pushshift API for more Reddit comments
- Working on hypertuning the features for LSTM to reduce RMSE as much as we can
  - Second Pass reduced RMSE!
  
![second_pass](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/second_attempt_lstm.png)
- Did a Y Test vs Y Pred

![ytest_ypred](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/y_vs_yhat.png)

So turns out that I made a mistake in the LSTM code that made the feature a response ... :( I was so happy about the results

This is the results after I fixed it 
![sad_results](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/sad_results.png)

![sad](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/sad_y_vs_yhat.png)

![sad_full_graph](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/sad_full_y_vs_yhat.png)



###  Presentation Link:

https://docs.google.com/presentation/d/13kG7TohxFgR38zHCjTAdx-rxu92opvpIMzdI3tGLogI/edit?usp=sharing
