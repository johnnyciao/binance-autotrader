Autotrader V1.0

An easy to understand python-based software to trade cryptocurrencies on the Binance trading platform. It was based on the work of yusun_yaku. I've seen it being capable of making fantastic profits. However it is important to choose the right strategy for every market / situation. And it is not easy to outperform the buy-and-hold strategy.

When writing this code, I focused on accessibility. For this reason I left out almost all object-oriented abstractions and used global variables. Every person who understands the very basics of programming and is able to follow the steps below, will understand this code and can try out his own strategy. Also, the framework for the trading itself has been provided and takes over all the work, so that the user can focus on strategies.

The following features have already been implemented and can be used right away:

- Scan all markets and find the market which is most likely to move in an upward direction (either based on MACD-value, price appreciation or both)

- MACD
    * Use MACD value of wider time interval to predict profitability
    * Use MACD Hist value to determine the best moment to buy
    * Sell when Hist value is decreasing so at the maximum or when a certain percentage of profit has been reached

- Bollinger Bands
    * Detect movement to and from a band and inbetween
    * Buy when leaving lower band, sell when leaving upper band

- EMA
    * Buy when ema 9 > ema 20
    * Sell when ema 9 < ema 20

- best combined strategies
    * Buy cheap based on Bollinger Bands
    * Sell high based on MACD Hist value

- Other TA strategies can easily be implemented

- Predicting the next value with AI Recurrent Neural Network

- Let an agent decide when to buy and sell (deep Q reinforcement learning)

- Test mode

- Sell at best price possible

- Profit from quick movements / Sell quickly at price drops

Still on roadmap:

- Backtesting a strategy

- Automatic sell when price of BTC drops too fast


New strategies can be added as well in a simple and down-to-earth way (just follow the steps below).

How to install

1. clone this repository

2. install required packages using pip install -r requirements.txt

3. You will need a Binance account, so please sign up using the following link:

4. After signing up, head over to the API part and get your secret key and password. Handle them with care. Paste them into config.py.

5. Now run python autotrader.py

   it should look like this:
   
   To learn how to use this trader, please have a look at config.py
   
   (explanation)
   
6. Creating your own strategy

In order to create your own strategy, you create a copy of the file strategy.py and change the rules according to your needs. You update the strategy variable in config.py
and it will work according your rules.

7. Collaborate

If you discover working strategies, please upload them to this repository, so everyone will profit from them.
   
8. Thank me

Please support me with some cryptos. I put a lot of effort in this for you. If you have no money, you can sign up at keybase.io to get free cryptos every month and then send me some. Thank me later!

Warning: trading is risky and you could lose money. I advise to never deactivate the test mode unless you have a strategy which always works or makes profits on the longer run.
