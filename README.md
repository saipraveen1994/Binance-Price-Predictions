# Binance-Price-Predictions
CS6313 - Statistical Methods for Data Science Graduate Project

# Token Data sets
## 1. networkbnbTX.txt (Token edge Data)
Token edge files have this row structure: fromNodeID\ttoNodeID\tunixTime\ttokenAmount\r\n
This row implies that fromNodeID sold tokenAmount of the token to toNodeID at time unixTime. 
fromNodeID and toNodeID are people who invest in the token in real life; 
each investor can also use multiple addresses. Two addresses can sell/buy tokens multiple times with multiple amounts. 
For this reason, the network is considered a weighted, directed multi(edge) graph. 
Each token has a maximum token count maxt; you can think of maxt as the total circulating token amount.

## 2. binance.txt (Price Data)
Price files have this row structure: Date\tOpen\tHigh\tLow\tClose\tVolume\tMarketCap\r
The price data is taken from https://coinmarketcap.com/. Open and close are the prices of the specific token at the given date. 
Volume and MarketCap give total bought/sold tokens and market valuation at the date.

## Token supply and sub-unit definitions
Token has a limited supply (i.e., token count, which can be found on coinmarketcap.com as circulating amount). Then each token may have sub-units. This idea comes from Bitcoin where subunits are called Satoshis, 1 Bitcoin =108 satoshis. Coin market cap gives the total supply, but not sub-units, which differ from token to token. Some tokens have 1018 sub-units. That means there can be numbers as big as totalAmount∗1018.

## Project - 1
Question 1
Find the distribution of how many times a user 1 - buys, 2 - sells a token. Which discrete distribution type fits these distributions best? Estimate distribution parameters.

Question 2
How can we create layers of transactions with increasing amounts? This descriptive statistic is similar to bin selection in histograms. For example, we could choose layer1 as those transactions that involve 0.01×maxt in amount. Find a good value for the number of layers and justify your choice. Find an algorithm to compute the correlation of price data with each of the layers (hint: start by looking at Pearson correlation).

## Project - 2
## Predicting the closing price using Multiple Linear Regression Model

In this regression model, we are predicting the price because we are using yesterday’s features to predict today’s price. This prediction model can be trained on the first 80% days, and used to predict the price of last 20% of data. In predictions we use the root mean square error to test model performance.
