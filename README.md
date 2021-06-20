# ![logo](images/Pine.png "Pine")

## Stochastic Oscilators

## Summary 💊

This is a collection of Stochastic indicators.
It's developed in PineScript for the technical analysis platform of **TradingView**.

## Motivation 💊

Here I developed some customized versions of *Stochastic Oscilators*.
Basically, I took a lot of interesting ideas from various authors, and put them all together.
Implementations:
  
1. Script developed in PineScript 4
2. Possibility to choose two themes ("Deep Purple" and "Blue and Red")
3. Possibility to choose the type of moving average applied to both indicator and signal
4. Histogram with gradient colors, emphasizing the strength of momentum
5. Crossover and crossunder signs
6. Coloring bars like the histogram
7. Background fill between indicator and signal lines

Each indicator has it's own defaults.
For example, in SMI (Stochastic Momentum Index) the indicador and signal lines uses the Exponential Moving Average (EMA).
Here we can choose them.

In this script, the following moving averages can also be used:

- Simple (SMA)
- Exponential Moving Average (EMA)
- Double Exponential (DEMA)
- Triple Exponential (THEME)
- Weighted (WMA)
- Smoothed (SSMA)
- Least Squares (LSMA)
- Hull
- Arnaud Legoux

There are 256 possibilities...

Example:

![alt](image/../images/New%20SMI.png)

## Caution 💊

No technical indicators are 100% accurate as they can sometimes generate false signals.

You should never rely on a single indicator and always use a range of them when making trading decisions.

---

## How to use this tool 💊

Place the indicator in TradingView. Than simply choose the parameters.

---

## Definitions 💊

### 1. What is "Stochastic"?

Generally speaking, a process can be defined as *stochastic* when a set of random variables *x* produce a set of random results *y*, and the results of *y*, although random, can be segable sequentially of time.

Examples of stochastic processes:

- fluctuations in stock markets and exchange rates;
- medical data such as temperature, blood pressure, data from an electroencephalogram;
- turbulent flow of a liquid or gas;
- variations in the Earth's magnetic field.

### 2. What is the "Stochastic Oscilator"?

The Stochastic Oscillator (STOCH) was developed by George Lane in the 1950's.

The stochastic oscillator was designed to indicate when a market becomes overbought or oversold within a trading range.
The indicator produces readings between zero and 100.

The first line (known as %K) displays the current close in relation to a user-defined period's high/low range.
The second line (known as %D) is a simple moving average of the %K line.
Now, as with most indicators, all of the periods used within Stochastic can be user defined.
That being said, the most common choices are a 14 period %K and a 3 period SMA for %D.

So, the stochastic indicator (%K) is calculated as follows:

`%K = SMA(100 * (Current Close - Lowest Low) / (Highest High - Lowest Low), smoothK)`

where:

- Lowest Low = The lowest price within the number of recent bars in the look-back period (periodK input)
- Highest High = The highest price within the number of recent bars in the look-back period (periodK input)

And the second line (known as %D) is a simple moving average of the %K line.
It's serve to minimize whipsaws while remaining in the larger trend.

%D is calculated as follow:

`%D = SMA(%K, periodD)`

![Example of STOCH Oscilator](images/Stochast%20-%20Example.jpg)

### 2. What is *Stochastic Momentum Index (SMI) Ergodic* 📈

The Stochastic Momentum Index (SMI) is a more refined version of the stochastic oscillator, employing a wider range of values and having a higher sensitivity to closing prices.

While the original STOCH from 1950's is limited in range between 0 and 100, in SMI the range is expanded to -100 and 100.
So it can be negative or positive.

The SMI is considered a refinement of the stochastic oscillator.
It calculates the distance of the current closing price as it relates to the median of the high/low range of price.
William Blau developed the SMI, which attempt to provide a more reliable indicator, less subject to false swings.

![Example of Stochastic Momentum Index (SMI)](images/Stochast%20Momentum%20Index%20-%20Example.jpg)

### References 💊

- Stocks & Commodities V. 15:12 (561-564): The Stochastic Oscillator by Joe Luisi
- Stocks & Commodities V. 11:1 (11-18): Stochastic Momentum by William Blau
- [TradingView](https://br.tradingview.com)
- [Investopedia](https://www.investopedia.com/)

#### Donations

- ADA: addr1q88aepqmd0wcgpgl5zst74z6nfgd7vrct607l7aj96ml80vdejles9j9cd5gl0vthm5dpwcfq5ky0n3ud9yw4q3v96sqpz6a43
- BTC: 1PnerhP2C5xeGXxAkhxQX4rYrBUguGe1yh
- XLM: GCPONJ5OX7KSEHBNPB2SKJZJGYSXTRN7ORYQXW443BLEFLS72ZVYISG2
