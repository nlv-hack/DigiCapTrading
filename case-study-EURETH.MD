# Base position activity investigation

Multiple transactions were performed using DigiCap trading bot , this is to outline how the bot generated €29.83 in profit.

## The set up

* An initial transaction was added using the bot functionality to perform a BUY on the Kraken exchange; **0.02** ETH was purchased for **39.67** EUR.

* A simple strategy was set up using the bot instructing the bot engine to perform a BUY or a SELL action when the stock price indicated we would make 0.05% profit, e.g. if the stock price is equal to 39.67 + 39.67 * 0.05 it will perform an action as that would yeld 0.05% profit. Same with BUY - if the bot can make 0.05% more ETH with the EUR funds it aquired earlier - it will perform that action.

## The data

Below transactions are RAW records that show how bot reacted to stock price changes and what actions it performed when strategy conditions were met

|LastStatusChangeTime                |Out       |In        |StockPrice|Fee|Profit |Misc|FIELD8|AssetPairCode                                                             |FIELD10 |Type   |
|------------------------------------|----------|----------|----------|---|-------|----|------|--------------------------------------------------------------------------|--------|-------|
|12/06/2021 17:39:07.183             |39.67 EUR |0.02 ETH  |1978.75   |0.1|0      |Bot bought 0.02 ETH for 39.67 EUR. We made 0.00 EUR.|      |XETHZEUR                                                                  |        |0      |
|12/06/2021 22:22:45.924             |0.02 ETH  |39.88 EUR |1999.23   |0.1|0.21   |Bot sold 0.02 ETH for 39.88 EUR. We made 0.210000000000000000 EUR.|      |XETHZEUR                                                                  |        |1      |
|13/06/2021 01:04:12.057             |39.99 EUR |0.02016779 ETH|1978.12   |0.1|0.32   |Bot bought 0.02016779 ETH for 39.99 EUR. We made 0.320000000000000000 EUR.|      |XETHZEUR                                                                  |        |0      |
|13/06/2021 02:48:03.997             |0.02016779 ETH|40.27 EUR |2001.91   |0.1|0.6    |Bot sold 0.02016779 ETH for 40.27 EUR. We made 0.600000000000000000 EUR.|      |XETHZEUR                                                                  |        |1      |
|13/06/2021 17:54:18.867             |40.37 EUR |0.02032206 ETH|1981.96   |0.1|0.7    |Bot bought 0.02032206 ETH for 40.37 EUR. We made 0.700000000000000000 EUR.|      |XETHZEUR                                                                  |        |0      |
|16/06/2021 16:52:21.517             |0.02032206 ETH|40.6 EUR  |2002.92   |0.1|0.93   |Bot sold 0.02032206 ETH for 40.6 EUR. We made 0.930000000000000000 EUR.|      |XETHZEUR                                                                  |        |1      |
|16/06/2021 17:38:08.351             |40.69 EUR |0.02048218 ETH|1982.03   |0.1|1.02   |Bot bought 0.02048218 ETH for 40.69 EUR. We made 1.020000000000000000 EUR.|      |XETHZEUR                                                                  |        |0      |
|16/06/2021 18:10:57.010             |0.02048218 ETH|40.9 EUR  |2001.88   |0.1|1.23   |Bot sold 0.02048218 ETH for 40.9 EUR. We made 1.230000000000000000 EUR.|      |XETHZEUR                                                                  |        |1      |
|16/06/2021 18:13:11.952             |40.94 EUR |0.02064155 ETH|1978.73   |0.1|1.27   |Bot bought 0.02064155 ETH for 40.94 EUR. We made 1.270000000000000000 EUR.|      |XETHZEUR                                                                  |        |0      |
|16/06/2021 23:03:05.404             |0.02064155 ETH|41.18 EUR |2000.09   |0.1|1.51   |Bot sold 0.02064155 ETH for 41.18 EUR. We made 1.510000000000000000 EUR.|      |XETHZEUR                                                                  |        |1      |
|17/06/2021 00:30:23.452             |41.27 EUR |0.02079797 ETH|1979.81   |0.1|1.6    |Bot bought 0.02079797 ETH for 41.27 EUR. We made 1.600000000000000000 EUR.|      |XETHZEUR                                                                  |        |0      |
|17/06/2021 17:11:12.996             |0.02079797 ETH|41.49 EUR |1999.76   |0.1|1.82   |Bot sold 0.02079797 ETH for 41.49 EUR. We made 1.820000000000000000 EUR.|      |XETHZEUR                                                                  |        |1      |
|04/07/2021 21:41:35.229             |41.57 EUR |0.02096057 ETH|1978.87   |0.1|1.9    |Bot bought 0.02096057 ETH for 41.57 EUR. We made 1.900000000000000000 EUR.|      |XETHZEUR                                                                  |        |0      |
|04/07/2021 22:49:28.761             |0.02096057 ETH|41.9 EUR  |2003.99   |0.1|2.23   |Bot sold 0.02096057 ETH for 41.9 EUR. We made 2.230000000000000000 EUR.|      |XETHZEUR                                                                  |        |1      |
|07/07/2021 09:49:27.669             |41.98 EUR |0.02119136 ETH|1976.74   |0.1|2.31   |Bot bought 0.02119136 ETH for 41.98 EUR. We made 2.310000000000000000 EUR.|      |XETHZEUR                                                                  |        |0      |
|07/07/2021 15:36:20.380             |0.02119136 ETH|42.5 EUR  |2010.75   |0.11|2.83   |Bot sold 0.02119136 ETH for 42.50 EUR. We made 2.830000000000000000 EUR.|      |XETHZEUR                                                                  |        |1      |
|07/07/2021 18:15:55.416             |42.61 EUR |0.02142147 ETH|1984      |0.11|2.94   |Bot bought 0.02142147 ETH for 42.61 EUR. We made 2.940000000000000000 EUR.|      |XETHZEUR                                                                  |        |0      |
|07/07/2021 22:08:37.585             |0.02142147 ETH|42.82 EUR |2004.31   |0.11|3.15   |Bot sold 0.02142147 ETH for 42.82 EUR. We made 3.150000000000000000 EUR.|      |XETHZEUR                                                                  |        |1      |
|07/07/2021 22:08:37.449             |42.93 EUR |0.02158494 ETH|1983.91   |0.11|3.26   |Bot bought 0.02158494 ETH for 42.93 EUR. We made 3.260000000000000000 EUR.|      |XETHZEUR                                                                  |        |0      |
