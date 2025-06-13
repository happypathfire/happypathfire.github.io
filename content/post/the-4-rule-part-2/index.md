---
title: "The 4% Rule - part 2"
date: 2019-12-25
categories: 
  - "concepts"
tags: 
  - "4-rule"
  - "finanical-independence"
  - "fire"
  - "retirement"
  - "safe-withdrawal-rate"
---

# Flaws in the _Rule_ - Understanding the shortcomings of the 4% Rule

This is the second in the series of articles on the 4% Rule. If you have missed out on the first you can find it [here](https://happypathfire.com/the-4-rule-part-1/).

In the first article of the series I introduced the historical origins of the 4% Rule. The **Bengen Study** and the **Trinity Study** (_B&T Study or should I say BTS (k-pop :P)_). I summarized the results and the key recommendations for retirement planning or the _Safe Withdrawal rates_ in particular. In case you would like to further investigate the original sources then I have linked both research studies in that article.

In the previous article I briefly mentioned the problems with the methodology of the two studies which have become the cornerstone of retirement planning through the so called **4% _Rule_**_._

In this article I will try to dive deep and provide a more detailed analysis of the _flaws_ in the methodology used in the two studies. I will also propose an alternative approach that would be a better and much more realistic model of the future using modern simulation techniques. Like always these set of articles are going to be academic in nature, so once again grab your favorite beverage of choice...i’ll wait.

## Using the Past to Predict the Future

In almost all statistical methodologies the predictions of the future are based on past data. Let us venture out of the financial world for a moment and take much more broader perspective. Take the **Tesla FSD** - Full Self-Driving for example. The FSD system uses the past data in the form of information collected on hundreds of thousands of Tesla Vehicles on Millions of miles every single day and use it to train a model, in this case a Deep Neural Network model to predict the next best action. 

Even the simple weather predictions that we receive everyday and take for granted is based on millions of data points collected over centuries to build climate models that use past data to predict the future.

## The B&T Study Methodology

Coming back to the B&T Study the methodology used is _similar_, at least at the high level.

In both studies the authors look at historical returns data over a period of about **80~100 years**. They use broad based stock index like the S&P 500 index to represent the returns from stocks and a Government or High Quality corporate Bond Fund Indices to represent returns from Bonds. 

They look at the past data to check how often has a portfolio survived given a fixed withdrawal rate over a given retirement period. For example, with a 4% withdrawal rate over a 30 year period how often has the portfolio survived.

Survival is defined as the outcome where at the end of the 30 year Retirement period the value of the portfolio is **_greater than zero_**.

For example, if for the given scenario i.e. In a 100% Stock only portfolio with a 4% withdrawal over a 30 year period results in a total of 100 such scenarios using the past data and it is found that 98 portfolios survive i.e. the ending value of the portfolios are greater than zero then the survival rate is said to be 98/100 i.e. 98%.  

Now that we have a broad understanding of the B&T Study me dive deep into some of the short comings.

## Not enough practice

Without getting into the nitty-gritties of statistical analysis the general idea is that the **_more past data you have the better your ability to predict the future_**. 

The methodology used in the B&T Study is called the ‘**Rolling-Window**’ Method. In this method a scenario is built using a Window of data-points, returns in this case. The next scenario is the same window size but shifted by 1 period, a year in this case.

For example, the total period of the data set is from 1926 -1995, a period of 70 years. For a 30 year retirement period, the first scenario or window is from 1926 to 1926+30 years i.e. 1956. The second scenario or window is from 1927 to 1927+30 i.e. 1957. 

So, how many 30 year scenarios are used in the B&T Study?

Less than 70 , the reason being that once we reach the window of 1965 - 1995 the next window of 1966 - 1996 has no data for 1996, this missing data was substituted by **historical average returns**!

Not an uncommon technique but the B&T Study is trying to predict the future based on only ~40 valid scenarios (_Scenario 1926-1956 to Scenario 1965-1995 have actual return data and the rest of the scenarios do not have data at the time of the study and were replaced with average historical returns_). This is a very small data-set to predict 30 years into the future!  

## Same sequence of returns

One of the biggest flaws of the B&T Study is the assumption that the future returns will have similar sequence of returns as the past. This is a very weak assumption at best. In my opinion it is an error. The authors used ~40 scenarios which are a sequence of returns and predict that the future returns will follow any one of these sequences or at least a similar sequence.

Not only that, but also the fact that the **Rolling Window** method means that there is a significant amount of overlap between scenarios. For example between any two consecutive scenarios 29 of the 30 returns overlap. All of this means that those 40 scenarios are _not as unique to begin with_.

## Why the sequence of returns matter?

Imagine Mr X  **_FIREs using the 4% Rule_** on a 1Million$ portfolio with an expected annual expense of 40,000$.

Unfortunately for Mr.X the stock market returns for the first 3 years has been -28%, -11%, -5%. These returns are within the range of what the market has performed in the past.

At the end of these 3 years Mr X’s portfolio is worth **600,000 $**. If Mr.X sticks to the 4% Rule religiously then he would be withdrawing 40,000$ inflation adjusted on a 600,000$ portfolio which is 7% of the current portfolio. In spite of the market performing well in subsequent years, having a few bad years early on can lead to failure.

One way to understand this imagine Mr Y, who wants to retire at the beginning of year 4, a time after the 3 years of bad returns. Mr Y also believes in the 4% Rule and unfortunately has only **600,000$** in assets. Going by the 4% Rule Mr Y **cannot FIRE**. Mr X is also in the same space as Mr Y in terms of the assets but having a bad sequence of returns early on means that his FIRE is **_turned off_**.

It is good to hope for the best sequence of returns but it is foolish to plan assuming a good sequence of returns. 

## What does all of this mean to the 4% Rule?

Two things. Firstly, the B&T Study is based on a very limited amount of data and second, the way that data is used is very limited.

There is very little anyone can do about the lack of data other than just waiting long enough (hope capitalism does not collapse in the meantime) or collect data from multiple alternate universes etc. None of which are practical.

But, we can do a better job on the way the past data is used and that is what I would like to propose.

## The Monte Carlo Method

<figure>

![](images/Dice-1.jpg)

<figcaption>

_God knows the outcome of Chance!_

</figcaption>

</figure>

The Monte Carlo Method has been around for a century at least and is used in diverse fields like Nuclear Physics, Finance, Engineering, AI etc. It is a statistical method that involves generating a huge set of scenarios based on some conditions and then inferring the system behavior by analyzing the outcomes based on the generated scenarios.

I will not go into the details of this method as that is not the main aim of this article. If interested to learn more I would recommend starting off on the [Wiki](https://en.wikipedia.org/wiki/Monte_Carlo_method) page.  

## Why Monte Carlo?

Let us take a step back and see how many sequences are actually possible. From a set of 70 annual returns selecting 30 annual returns (non sequentially) yields a number like this 22539340290692258087863249000000000000000000000000000000 or 2.25 x 10^55.

For context a single grain of sand has ~3 x 10^22  atoms in it. The above number is close to the number of atoms on planet earth!!!

If you are overwhelmed by the number of sequences possible vs the actual sequences used for the B&T study then you are not alone. 

Running through all the possible combinations of scenarios is computationally expensive and possibly not required. There is a short-cut, which is through **random sampling**.

Random Sampling is used in a variety of industries. For example, quality control checks on manufactured parts is conducted through random sampling and then tested for defects. The main idea is that with a sufficiently large sample we can make fairly accurate predictions about the complete data set.

## Same-same but different - My Approach

Below is the approach I took at a high-level. It gives you an overview of the steps involved in the analysis.

I started off with  92 years of past annual returns of the S&P 500 index. I randomly sampled 30 returns in no particular order. I arranged the sample into a 30 year sequence. I then checked the value of the portfolio at the end of this **_generated 30 year_** period. I repeated this exercise for 10,000 times i.e. **10,000 Scenarios** (_not ~40 like in the B&T Study_) and then checked what percentage of those 10,000 scenarios actually survived.

In the next Article I will share the results from this Approach.
