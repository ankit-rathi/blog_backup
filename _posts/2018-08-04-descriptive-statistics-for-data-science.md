---
toc: true
layout: post
description: Probability & Statistics for Data Scientists
categories: [markdown]
title: Descriptive Statistics for Data Science
---

![Descriptive Statistics for Data Science](https://cdn-images-1.medium.com/max/1200/1*x9P63tACwb3o5wAL1MzLgQ.png)

*This is the 3rd post of blog post series ‘*[*Probability & Statistics for Data Science*](https://www.ankitrathi.com/post/probability-statistics-for-data-science-series)*’, this post covers these topics related to descriptive statistics and their significance in data science.*

-   *Introduction to Statistics*
-   *Descriptive Statistics*
-   *Uni-variate Analysis*
-   *Bi-variate Analysis*
-   *Multivariate Analysis*
-   *Function Models*
-   *Significance in Data Science*

------------------------------------------------------------------------

> Visit [ankitrathi.com](http://ankitrathi.com/) now to:

> — to read my blog posts on various topics of AI/ML

> — to keep a tab on latest & relevant news/articles daily from AI/ML world

> — to refer free & useful AI/ML resources

> — to buy my books on discounted price

> — to know more about me and what I am up to these days

**Statistics Introduction**

*Statistics* is a mathematical body of science that pertains to the *collection*, *analysis*, *interpretation* or *explanation*, and *presentation* of data.

![Informal definition :D](https://cdn-images-1.medium.com/max/800/1*D7SIHTCAhCeuWxZA778M2g.png)

*Statistics*, in short, is the study of data. It includes *descriptive statistics* (the study of methods and tools for collecting data, and mathematical models to describe and interpret data) and *inferential statistics* (the systems and techniques for making probability-based decisions and accurate predictions.

![Descriptive Vs Inferential Statistics](https://cdn-images-1.medium.com/max/800/1*7BFPt6R298dJeTsh3oEjLg.png)

**Population vs Sample**

Population means the aggregate of all elements under study having one or more common characteristic while *sample* is a *part of population* chosen at random for participation in the study.

![Population Vs Sample](https://cdn-images-1.medium.com/max/800/0*53aOxE5IP8p0gcH7.jpg)

**Descriptive Statistics**

A descriptive statistic is a summary statistic that quantitatively describes or summarizes features of a collection of information. Descriptive statistics are just descriptive. They do not involve generalizing beyond the data at hand.

**Types of Variable**

*Dependent and Independent Variables:* An independent variable (experimental or predictor) is a variable that is being manipulated in an experiment in order to observe the effect on a dependent variable (outcome).

![Other names of variables](https://cdn-images-1.medium.com/max/800/1*dSVkJMtF2au-nxH9sauxow.png)

*Categorical and Continuous Variables:* Categorical variables (*qualitative*) represent types of data which may be divided into groups. Categorical variables can be further categorized as either *nominal, ordinal* or *dichotomous*. Continuous variables (*quantitative*) can take any value. Continuous variables can be further categorized as either *interval or ratio* variables.

![*Categorical Vs continuous variables*](https://cdn-images-1.medium.com/max/800/1*z_7tcnFTKTbKXg-jxxuUYA.png)

**Central Tendency**

Central tendency is a *central* or *typical* value for a distribution.It may also be called a *center* or *location* of the distribution. The most common measures of central tendency are the arithmetic *mean*, the *median* and the *mode*.

![Mean, median & mode as Central Tendency](https://cdn-images-1.medium.com/max/800/0*e6O85dyjyHSBQyH2.jpg)

*Mean* is the numerical average of all values, *median* is directly in the\
middle of the data set while *mode* is the most frequent value in the data set.

**Spread or Variance**

Spread (dispersion or variability) is the extent to which a distribution is stretched or squeezed. Common examples of measures of statistical dispersion are the *variance*, *standard deviation*, and *inter-quartile range (IQR)*.

![Spread or Variance](https://cdn-images-1.medium.com/max/800/0*CLX1QEZn7IHxp7q8.png)

*Inter-quartile range* (IQR) is the distance between the 1st quartile and 3rd quartile and gives us the range of the middle 50% of our data. *Variance* is the average of the squared differences from the mean while *standard deviation* is the square root of the variance.

*Upper outliers: Q3+1.5 ·IQR\
Lower outliers: Q1–1.5 ·IQR*

*Standard Score or Z score:* For an observed value x, the Z score finds the number of standard deviations x is away from the mean.

![Standard deviation & Z-score](https://cdn-images-1.medium.com/max/800/1*UObdAoIcg3HKTSXC3kwtXg.png)

The *Central Limit Theorem* is used to help us understand the following facts regardless of whether the population distribution is normal or not:\
1. the *mean* of the sample means is the same as the population mean\
2. the *standard deviation* of the sample means is always equal to the *standard error*.\
3. the *distribution* of *sample means* will become increasingly more *normal* as the sample size increases.

**Uni-variate Analysis**

In uni-variate analysis, appropriate statistic depends on the level of measurement. For *nominal variables*, a frequency table and a listing of the mode(s) is sufficient. For *ordinal variables* the median can be calculated as a measure of central tendency and the range (and variations of it) as a measure of dispersion. For *interval level variables*, the arithmetic mean (average) and standard deviation are added to the toolbox and, for *ratio level variables*, we add the geometric mean and harmonic mean as measures of central tendency and the coefficient of variation as a measure of dispersion.

For interval and ratio level data, further descriptors include the variable’s *skewness* and *kurtosis*. *Skewness* is a measure of symmetry, or more precisely, the *lack of symmetry*. A distribution, or data set, is symmetric if it looks the same to the left and right of the center point. *Kurtosis* is a measure of whether the data are *heavy-tailed* or *light-tailed* relative to a normal distribution.

![Skewness & Kurtosis](https://cdn-images-1.medium.com/max/800/1*CAnSVnnI3JJ1gL_hrHJJ1w.png)

Mainly, *bar graphs*, *pie charts* and *histograms* are used for uni-variate analysis.

![Histogram, Pie-chart & Bar-graph](https://cdn-images-1.medium.com/max/800/1*IVh-UihQ8bZpfUdjEzigUg.png)

**Bi-variate Distribution**

Bivariate analysis involves the analysis of two variables (often denoted as X, Y), for the purpose of determining the empirical relationship between them.

For two continuous variables, a *scatter-plot* is a common graph. When one variable is categorical and the other continuous, a *box-plot or violin-plot (*also *Z-test* and *t-test)* is common and when both are categorical a *mosaic plot* is common (also *chi-square test*).

![Box-plot, Scatter-plot, Mosaic-plot & Violin-plot](https://cdn-images-1.medium.com/max/800/1*qANiG_SwpMB8TYM1916aTw.png)

![z & t-Tests](https://cdn-images-1.medium.com/max/800/1*VM0z3L6eKOesSr2C3xXA7A.png)

**Multi-variate Analysis**

Multi-variate analysis involves observation and analysis of more than one statistical outcome variable at a time. *Multi-variate scatter plot*, g*rouped box-plot (or grouped violin-plot*), *heat-map* are used for multi-variate analysis.

![Multi-variate scatter-plot, Grouped box-plot, Grouped violin-plot, Heat-map](https://cdn-images-1.medium.com/max/800/1*1SpYTGYkndWUxDIlWUXhkw.png)

**Function Models**

A **function** can be expressed as an equation, as shown below. In the equation, f represents the *function* name and x represents the *independent* variable and y represents the *dependent* variable.

![A typical function](https://cdn-images-1.medium.com/max/800/1*RyiSC9L6UQkz1y8c-hU8dw.png)

A **linear function** has the same average rate of change on every interval. When a linear model is used to describe data, it assumes a constant rate of change.

![Linear function](https://cdn-images-1.medium.com/max/800/1*SQdxEysedW-qYicyWXD3YA.png)

**Exponential functions** have variable appears as the exponent (or power) instead of the base.

![Exponential functions](https://cdn-images-1.medium.com/max/800/1*GwwJU63W8zZA8YdTIOYRyg.png)

The **logistic function** has effect of limiting upper bound, a curve that grows exponentially at first and then slows down and hardly grows at all.

![Logistic functions](https://cdn-images-1.medium.com/max/800/1*vvXZqzfG1_ajNUpYeFIT0g.png)

**Significance in Data Science**

Descriptive Statistics helps you to understand your data and is initial & very important step of Data Science. This is due to the fact that Data Science is all about making predictions and you can’t predict if you can’t understand the patterns in existing data.

**References:**

\[embed\]https://classroom.udacity.com/courses/ud827-india\[/embed\]\
\[embed\]https://classroom.udacity.com/courses/ud827-india\[/embed\]

------------------------------------------------------------------------

[*Ankit Rathi*](https://www.ankitrathi.com/) *is an AI architect, published author & well-known speaker. His interest lies primarily in building end-to-end AI applications/products following best practices of Data Engineering and Architecture.*

*Why don’t you connect with Ankit on* [*YouTube*](https://www.youtube.com/channel/UCrIv4EU2tFX8VhhT0oCnDnw)*,* [*Twitter*](https://twitter.com/rathiankit)*,* [*LinkedIn*](https://www.linkedin.com/in/ankitrathi/) *or* [*Instagram*](https://instagram.com/ankitrathi/)*?*
