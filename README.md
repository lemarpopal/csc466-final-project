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

Presentation Link:

https://docs.google.com/presentation/d/13kG7TohxFgR38zHCjTAdx-rxu92opvpIMzdI3tGLogI/edit?usp=sharing
