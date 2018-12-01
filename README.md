# Binance-Price-Predictions
CS6313 - Statistical Methods for Data Science Graduate Project

# Token Data sets
1. networkbnbTX.txt (Network Data)
Token edge files have this row structure: # fromNodeID\ttoNodeID\tunixTime\ttokenAmount\r\n #
This row implies that fromNodeID sold tokenAmount of the token to toNodeID at time unixTime. 
fromNodeID and toNodeID are people who invest in the token in real life; 
each investor can also use multiple addresses. Two addresses can sell/buy tokens multiple times with multiple amounts. 
For this reason, the network is considered a weighted, directed multi(edge) graph. 
Each token has a maximum token count maxt; you can think of maxt as the total circulating token amount.

2. binance.txt (Price Data)
Price files have this row structure: # Date\tOpen\tHigh\tLow\tClose\tVolume\tMarketCap\r #
The price data is taken from https://coinmarketcap.com/. Open and close are the prices of the specific token at the given date. 
Volume and MarketCap give total bought/sold tokens and market valuation at the date.


