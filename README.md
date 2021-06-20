# ![logo](images/Pine.png "Pine")

## Stochastic Oscilators

## Summary 💊

This is a collection of Stochastic indicators.
It's developed in PineScript for the technical analysis platform of **TradingView**.

## Motivation 💊

Here I developed a customized version of *Stochastic Momentum Index (SMI) Ergodic*.
Basically, I took a lot of interesting ideas from the authors mentioned above, and put them all together.
Implementations:
  
1. Script developed in PineScript 4
2. Possibility to choose two themes
3. Possibility to choose the type of moving average applied to both the SMI indicator and the signal
4. Histogram with gradient colors, emphasizing the strength of momentum
5. Crossover and crossunder signs
6. Coloring of the bars like the histogram
7. Background fill between indicator and signal lines

By default, the SMI and Signal lines uses the Exponential Moving Average (EMA).

In this script, the following moving averages can also be used:

- Simple (SMA)
- Double Exponential (DEMA)
- Triple Exponential (THEME)
- Weighted (WMA)
- Smoothed (SSMA)
- Least Squares (LSMA)
- Hull
- Arnaud Legoux

There are 256 possibilities...

## Caution 💊

No technical indicators are 100% accurate as they can sometimes generate false signals.

You should never rely on a single indicator and always use a range of them when making trading decisions.

---

## How to use this tool 💊

Place the indicator in TradingView. Than simply choose the parameters.

---

## Definitions 💊

### 1. What is "Stochastic"?

Genericamente falando, um processo pode ser definido como *estocástico* quando um conjunto de variáveis aleatórias *X* produzem um conjunto de resultados aleatórios *Y*, e os resultados de *Y*, embora aleatórios, podem ser ordenados de forma sequencial ao longo do tempo.

Exemplos de processos estocásticos:

- flutuações nos mercados de ações e nas taxas de câmbio;
- dados médicos como temperatura, pressão sanguínea, dados de um eletroencefalograma;
- fluxo turbulento de um líquido ou gás;
- variações no campo magnético da Terra.

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

![- %D is a smoothed average of %K,](images/Stochast%20-%20Example.jpg)

### 2. What is *Stochastic Momentum Index (SMI) Ergodic* 📈

The Stochastic Momentum Index (SMI) is a more refined version of the stochastic oscillator, employing a wider range of values and having a higher sensitivity to closing prices.

The SMI is considered a refinement of the stochastic oscillator. It calculates the distance of the current closing price as it relates to the median of the high/low range of price. William Blau developed the SMI, which attempt to provide a more reliable indicator, less subject to false swings.

The SMI has a normal range of values between +100 and -100.

![- %D is a smoothed average of %K,](images/Stochast%20Momentum%20Index%20-%20Example.jpg)

### References 💊

- TradingView
- Stocks & Commodities V. 11:1 (11-18): Stochastic Momentum by William Blau
