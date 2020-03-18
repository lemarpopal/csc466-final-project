# Anish Yakkala

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
- Factorize all my functions in the Sentiment Analysis to make it completely reproducible for any ticker
- Begin thinking of what ML models we will be using on our data with Financial Action indicator columns and historical stock data


### Week 2 (3/03/2020 - 3/10/2020)

- Expand on the Sentiment Analysis Alogrithm from https://github.com/theriley106/TheWSBIndex
- Looked at how upvote history fits with various features corresponding to financial movement
![score_vs_volume](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/volume_vs_score.png)
- Made a simple Exponential Moving Average Algorithm to fit onto our data
![moving_average](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/Exponential_Moving_Average.png)
- Fit a LSTM model onto our dataset with the features derived from the Sentiment Analysis Algorithm. (Focused on TSLA)
![first_pass](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/first_attempt_lstm.png)
- Working on hypertuning the features for LSTM to reduce RMSE as much as we can
  - Second Pass reduced RMSE!
  
![second_pass](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/second_attempt_lstm.png)
- Did a Y Test vs Y Pred

![ytest_ypred](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/y_vs_yhat.png)

![full_ytest_ypred](https://github.com/Anderson-Lab/final-project-dennis-sun/blob/master/images/fully_vs_yhat.png)

- Read more about how LSTM works and how it predicts. This was a big point of confusion for me.
