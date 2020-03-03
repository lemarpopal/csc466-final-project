# Lemar Popal

### Week 1 (02/25/2020-03/02/2020)
Wrote some Python code to get data from the Pushshift API. I originally wanted to get all comments for 2019, but I was only able to get about 31,500 comments (about 4 days worth of comments) before the API would started acting weird. So if there was error I would catch the it and continue the loop. I was able to get a week's worth of comments within a few minutes. Extrapolating for the entire year, there would be about 3 million comments total. This is roughly the same amount of comments between 2012 and 2018 (from the Kaggle dataset), so Wall Street Bets had a lot more activity in 2019 alone. 

I also worked with Anish and Adrien on the data exploration for the data we found on Kaggle. We looked at another repository (linked in the README) that did some preliminary analysis of comments from the data. In there was a useful algorithm that went through each comment and extracted the indicated position towards each stock ticker in a comment (puts, calls, buy, sell). Then did some visualization to see if the the number of puts, calls, buys, and sells in comments for Tesla was correlated to the actual performance of the stock. 


