## Week 1

For the presentation I found the dataset that we ended up using (which led to use finding the helpful repo). I helped write our moviations behind our project and what sorts of questions we want to ask.

Together our group went over the repo linked in our README to understand how to use the Reddit dataset and started to create our own EDA to get prepare our Reddit comments for later training when we get to applying the ML models. Anish started with a simple sentiment detection method but I found in the repo a helpful function that does much more complex language processing, which we ended up using to determine whether the Reddit comments wanted to Buy, Sell, Call, or Put the given stock. I helped determine the features we want to start training our ML model with. I also had a big part in deciding which model(s) we want to start with, namely a Random Forest Regressor and Gradient Boost (possibly XGBoost). I decided that we should use these methods because we wanted to start with models we had discussed and implemented in class.


## Week 2

This week I spent a lot of time pulling current comments from /r/wallstreetbets using the Pushshift API. Lemar and I did some individual work on it, just testing the limits of it and how viable of a data source it is, and then collaborated with Anish to make decisions on if we want to use the recent WallStreetBets data and what we want to do with it. I discovered that we can get 1000 comments per request, with a restriction of 120 calls per minute, which means we can get 120,000 comments per minute. Unfortunately Reddit has LOTS of comments, so it takes a while to get data for multiple months. I thought I had found a nice way to limit comments using a nest_level attribute of the api, which would limit how far down the comment chain the comment would come from, but it appears that the parameter doesn't work so we were back at square one.

I DM'd the creator of the API on Reddit but he has yet to respond to me so we'll see if I can figure that out.

I also pulled 6 months of Reddit comments from 2019 so we have another set of data to train/test on. Eventually we want to pull live(ish) data from Pushshift so that we can maybe try to predict near future stock prices (we'll see how succesful we are with this given the current market volatility). Then I uploaded the dataset to [Kaggle](https://www.kaggle.com/adrienchaussabel/wall-street-bets-comments-from-jan1-to-jun2) (Upvote pls)

## Week 3

I helped Lemar on the Naive ML methods where we tried out a Decision Tree, Random Forest, and Gradient Boost (XGBoost). We picked these methods because these are methods we implemented in class, so we know exactly how they work. We found little success in these methods with some pretty abysmal RMSE but it gives us a baseline for Anish's much better model which is specifically designed for this type of work.
