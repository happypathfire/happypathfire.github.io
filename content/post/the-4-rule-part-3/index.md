---
title: "The 4% Rule - part 3"
date: 2019-12-27
categories: 
  - "concepts"
tags: 
  - "4-rule"
  - "fat-fire"
  - "finanical-independence"
  - "fire"
  - "retirement"
---

# Results from my Study

_This is the second in the series of articles on the 4% Rule. If you have missed out on the first you can find it [here](https://happypathfire.com/the-4-rule-part-1/), the second can be found [here](https://happypathfire.com/the-4-rule-part-2/)._

In the first article I introduced the origins of the so called 4% Rule which is based on the Bengen and Trinity Study (B&T Study). I talked about those two studies in detail along with links to the source material for interested readers. 

In the second part of the series I tried to show some of the flaws of the studies and proposed an alternative - The Monte Carlo Method.

In this article I present some of the results from applying these methods. Like all articles in this series this one too is going to be fairly academic so please make yourself comfortable with a beverage of choice… I’ll wait.

## My Data-set

The Data that I use for the analysis are the annual returns in percentage terms on the S&P 500 Index. I chose the S&P Index as a proxy for a broad based Stock or Equity portfolio.

I have used data for the past 92 years starting off from the Year 1928 to Year 2019. At the time of this writing, I used the returns until the 20th of November 2019 Instead of 31st December like in all other annual returns.

<figure>

![](images/DWchjMJzwNCagvP5iXUzXEtZeeNjI2Szh0DYNKk_ZfUxLaB12u0VgmBVXZAU26lQhidmCZddxZcbAoiWB5_baKmnNYf_fsH1_txamAbKVxq_BKYcqBCRYL9RR_wXMpcRr7XRyIQ7)

<figcaption>

Annual Percentage Returns on the S&P 500 Index

</figcaption>

</figure>

The chart above shows the annual returns of the S&P 500 as bars on the Y-Axis with the Dates on the X-Axis. The dates on the X-Axis are ordered from 1928 to 2019. A quick visual inspection tells us that there are more bars **_above 0_** than **_below 0_** , thankfully that is :) 

The other thing to notice is the fact that there is **no particular trendline** _per se_ in the returns. This means that the returns are mostly random. I think this becomes visually more evident on a line graph as shown below.

<figure>

![](images/jVjuocU1LimI1dUByFXJUlOytKbSLPHFWIGZx5rk_bmvChVXoNcx79zXz4w4E7XpMNbzIqR9bRvoJD5De75WbWe8wBQ9MBAMIfvEaTfY1xOlDZYBE35XLWT2AvkIX2zVNQ3L8rsw)

<figcaption>

Looks like noise rather than a smooth wave or a pattern!

</figcaption>

</figure>

It is important to know the distribution of returns. The chart below shows the distribution of returns grouped into buckets of size 10% each. 

<figure>

![](images/mGwFBkUzRQPKjBh7TuRlQ8c19F85DZ945P2o3QoRV4cBm2eueD5BzlZo2WE-gyBBGLNCzAaeO-xGZ9Ae7HlZs3RlLdXppq_yN7iLOIcmpwQdZZGr547fGg11DwNTFBom4gVfA3uB)

<figcaption>

Most Returns are found between 0%-30%

</figcaption>

</figure>

You may notice that most of returns in the last 92 years have been in the range of 10%-20%. The next two most frequently occurring annual return ranges are between 0%-10% and 20%-30%. 

The distribution looks like the _bell-curve_ with the number of instances of annual returns decreasing as we move far away from the centre (Mean, Median). 

Now that we have taken a look at the data-set let us run some analyses on it.

## Just the Dollar Returns

Just to get started on the analysis, I ran a baseline scenario.

### Scenario 0 - 

1. Invest 2M$ 
2. Time period = 30 Years
3. No Withdrawals

I used the Monte-Carlo Simulation approach outlined in the [previous article](https://happypathfire.com/the-4-rule-part-2/). So from the basket of 92 returns, I randomly picked (_Assuming that any return is equally likely_) 30 returns and created a sequence of 30 annual returns. I calculated the annual returns on that 2M$s for each of the 30 Years and plotted the returns as a line graph. I repeated this exercise 10,000 times.

<figure>

![](images/4HDuoJRk4xeXsUNHp1Nxm-iqoUMKKslE4oBDyE5Mb4mHmMsnXjxsKuuojcuUjwuqpZ-rOCSCW-2yTMbt4MUJm6St491ILSzmeE7tvA2HIKubGBw74-tMCQ6dh81NGj4VW1GW70ha)

<figcaption>

Look at the bunch of lines rather than trying to trace an individual line

</figcaption>

</figure>

Please do not be overwhelmed by how busy and tangled the lines look, the point of plotting 10,000 lines is to give some visual feedback on the general trend. You can see that the average of the 10,000 scenarios at the end of year 30 should be somewhere between 0-50M$s.

### These are the calculated summary of the returns:

- The mean or the average Value of the Portfolio is **14.57M$s**
- The Max Value of the Portfolio is **223.58M$s**
- The Min Value of the Portfolio is **0.18M$s** (~180,000$s)

This basic scenario helps us to put all the upcoming scenarios into context. So, things are looking good so far. Putting in 2M$s and not withdrawing anything for the next 30 years does well, at least you would not go bankrupt even in the most worst case scenario out of a 10,000 Scenarios. This is great news indeed. 

## The 4% Rule

This is the scenario that you may be waiting for all along. The scenario of the 4% Rule. 

### Scenario 1 - 

1. Invest 2M$ 
2. Time period = 30 Years
3. Withdrawals = 4% (with 3% Annual Inflation Adjustments)

<figure>

![](images/Pk4FjewHT5nKR1ef4UHYG3kenqcKtxnHJA8z6qLbOx1-3gdUEvJhAlB3TVGjoLhvl9xHU-Y_fA6AxAK1X8j1j5LwpgIYI2kCJkNStGhbgG6OSDQrdTsyoAF0pTz7dllMBHTYbk5C)

<figcaption>

The plot of the simulation looks more spread out that Scenario 0. 

</figcaption>

</figure>

### These are the calculated summary of the returns:

- The Mean or the Average Value of the Portfolio is **3.77 M$s**
- The Median Value of the Portfolio is **1.23M$s**
- The Max Value of the Portfolio is **131.47M$s**
- The Min Value of the Portfolio is **\-22.54M$s**

So the numbers do not look so bad afterall, right? The average value of the Portfolio at the end of 30 years in spite of 4% withdrawals and 3% Inflation adjustment is an average of ~3.77M$s over 10,000 scenarios. Even the median or the central Value or the Middle value of the Portfolio over 10,000 scenarios is 1.23M$s.

But is it hurrah!!! To the 4% Rule then? Not quite. **Remember, the 98% number?** That was the survival rate in the B&T Study. The percentage of portfolios that survived over the period of 30 years. Survival as defined as the portfolio value not going below zero.

So, what percentage of portfolios survived in this simulation using the 4% Rule???

Well, surprise! It is not 98%, not even 90%

The Survival rate is a measly - **61.45%** **!!!!!!**

Let that sink in a bit! 

If you had followed the 4% Rule then there is only a little over 60% of a chance that your portfolio will survive. This number is so vastly different from the 98% of the B&T Study that I was in a state of disbelief for a long time. 

## Is there any other rule out there? Like the 3% Rule?

Just out of curiosity I checked for the portfolio Survival Rate

### Scenario 2 - 

1. Invest 2M$ 
2. Time period = 30 Years
3. Withdrawals = 3% (with 2% Annual Inflation Adjustments)

Does the Survival Rate Improve? Well it does improve, and by quite a bit actually. 

The Survival Rate with a 3% Withdrawal at 2% Annual Inflation Adjustment is **85.79%!!!**

This is fairly drastic, about 25% points of improvement!!!

So, If 3%Rule is better than the 4% Rule then the 2% Rule should be Rad!! Let’s  check it out.

## The 2% Rule!

### Scenario 3 - 

1. Invest 2M$ 
2. Time period = 30 Years
3. Withdrawals = 2% (with 2% Annual Inflation Adjustments)

The Survival Rate is…..   **96.09%!!!!**

There you have it! Something finally in the range of the B&T Study. Only a 2% Rule can realistically save the day it seems.

## What does it all mean to you?

**I think, blindly applying the 4% Rule depending on the B&T Study is a mistake**. The FIRE movement is quite recent and is often criticized as a bull-market phenomenon.

If we had say 5 years of bear markets then all of the hype might die away leaving behind only the ones that have FAT FIREd with rest of the FIREd people going back to a tough job market. 

My study showed that FAT FIRE with 2% and below withdrawal has a high (~96%) chance of success. Does that mean that FAT FIRE is the actual FIRE?  Does that mean that 2% Rule is the new 4% Rule? Honestly, I am not sure.

I have more questions than answers. Firstly, my study is not complete, I have not included bonds in my portfolio, may be having bonds with annual rebalancing can increase survival rates? (_Does not mean that my study is wrong, the B&T Study also had a case where they had 100% Stock portfolio, just like mine and still incorrectly showed a >98% survival rate!!!_)

If the Inflation adjusted withdrawals are to be 2% then it opens up different asset classes like the TIPS(Treasury Inflation Protected Securities), Gold, Real Estate etc. for discussion. Should these be part of the portfolio? If so, then how much? 

These and many other questions are on my TO-DO list for next year.

Stay tuned!!! Happy New Year 2020!!!
