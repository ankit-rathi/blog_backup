Title: Probability for Data Science
Date: 2018-08-01 01:57
Author: ankitrathi
Category: Uncategorized
Tags: Data Science, Machine Learning, Probability, Statistics
Slug: probability-for-data-science
Status: published

![Probability for Data Science](https://cdn-images-1.medium.com/max/1200/1*5LCxMECKCdbyOrZDMqdA4Q.png)

*This is the 2nd post of blog post series ‘*[*Probability & Statistics for Data Science*](https://www.ankitrathi.com/post/probability-statistics-for-data-science-series)*’, this post covers these topics related to probability and their significance in data science.*

-   *Introduction*
-   *Conditional Probability*
-   *Random Variables*
-   *Probability Distributions*

------------------------------------------------------------------------

> Visit [ankitrathi.com](http://ankitrathi.com/) now to:

> — to read my blog posts on various topics of AI/ML

> — to keep a tab on latest & relevant news/articles daily from AI/ML world

> — to refer free & useful AI/ML resources

> — to buy my books on discounted price

> — to know more about me and what I am up to these days

**What is probability?**

Probability is the chance that something will happen — how likely it is that some event will happen.

![*Courtesy:* [*https://www.mathsisfun.com/data/probability.html*](https://www.mathsisfun.com/data/probability.html)](https://cdn-images-1.medium.com/max/800/0*q3bbkWVlnMSGUixH.gif)

*Probability of an event happening* ***P(E)*** *= Number of ways it can happen* ***n(E)****/ Total number of outcomes* ***n(T)***

Probability is the measure of the likelihood that an event will occur. Probability is quantified as a number between 0 and 1, where 0 indicates impossibility and 1 indicates certainty.

**Why probability is important?**

Uncertainty and randomness occur in many aspects of our daily life and having a good knowledge of probability helps us make sense of these uncertainties. Learning about probability helps us make informed judgments on what is likely to happen, based on a pattern of data collected previously or an estimate.

\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]

**How Probability is used in Data Science?**

Data science often uses statistical inferences to predict or analyze trends from data, while statistical inferences uses probability distributions of data. Hence knowing probability and its applications are important to work effectively on data science problems.

\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]\
\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]

**What is Conditional Probability?**

Conditional probability is a measure of the probability of an event (some particular situation occurring) given that (by assumption, presumption, assertion or evidence) another event has occurred.

![Courtesy: <https://www.mathsisfun.com/data/probability-events-conditional.html>](https://cdn-images-1.medium.com/max/800/0*A_FcopnqXGd_bVVn.gif)

*The probability of event B given event A equals the probability of event A and event B divided by the probability of event A.*

\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]

**How conditional probability is used in data science?**

Many data science techniques *(i.e. Naive Bayes)* rely on Bayes’ theorem. *Bayes’ theorem* is a formula that describes how to update the probabilities of hypotheses when given evidence.

![](https://cdn-images-1.medium.com/max/800/1*c0PJICLo_oPqKODuKnSIHQ.png)

Using the Bayes’ theorem, its possible to build a learner that predicts the probability of the response variable belonging to some class, given a new set of attributes.

![](https://cdn-images-1.medium.com/max/800/1*n4D8BKlVCurNg1xKshTsxg.png)

\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]\
\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]

**What are random variables?**

A random variable is a set of possible values from a random experiment.

![Courtesy: <https://www.mathsisfun.com/data/random-variables.html>](https://cdn-images-1.medium.com/max/800/1*UzBn1v7XGb37h4m191vRMw.png)

A random variable (random quantity, aleatory variable, or stochastic variable) is a variable whose possible values are outcomes of a random phenomenon.

Random variables can be discrete or continuous. *Discrete random variables* can only take certain values while *continuous random variables* can take any value (within a range).

\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]

**What are probability distributions?**

The *probability distribution* for a random variable describes how the probabilities are distributed over the values of the *random variable*.

For a *discrete random variable*, *x*, the probability distribution is defined by a **probability mass function**, denoted by *f*(*x*). This function provides the probability for each value of the random variable.

For a *continuous random variable*, since there is an infinite number of values in any interval, the probability that a continuous random variable will lie within a given interval is considered. So here, the probability distribution is defined by **probability density function**, also denoted by f(x).

Both probability functions must satisfy two requirements:: (1) *f*(*x*) must be non-negative for each value of the random variable, and (2) the sum of the probabilities for each value (or integral over all values) of the random variable must equal one.

\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]

**What are the types of probability distributions?**

A **binomial distribution** is a statistical experiment that has the following properties: The experiment consists of n repeated trials. Each trial can result in just two possible outcomes. We call one of these outcomes a success and the other, a failure. The probability of success, denoted by P, is the same on every trial.

![Courtesy: <https://math.stackexchange.com/questions/2123873/is-the-maximum-of-a-probability-distribution-function-of-a-binomial-distribution>](https://cdn-images-1.medium.com/max/800/0*pjpaimDcpsjt3XTJ.png)

![](https://cdn-images-1.medium.com/max/800/1*zwIpdL3bPwKbwS9Op0-5wQ.png)

The **normal distribution**, also known as the **Gaussian distribution**, is a *probability distribution* that is symmetric about the mean, showing that data near the mean are more frequent in occurrence than data far from the mean. It has following properties:

-   The normal curve is symmetrical about the mean μ;
-   The mean is at the middle and divides the area into halves;
-   The total area under the curve is equal to 1;
-   It is completely determined by its mean and standard deviation σ (or variance σ2)

![Courtesy: <https://www.mathsisfun.com/data/standard-normal-distribution.html>](https://cdn-images-1.medium.com/max/800/1*zyTPAakqx94qDuS3fkmjfg.png)

For other common *probability distributions*, please refer following links:

\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]\
\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]

**How random variables & probability distributions are used in data science?**

Data science often uses *statistical inferences* to predict or analyze trends from data, while statistical inferences uses *probability distributions* of data. Hence knowing *random variables* & their *probability distributions* are important to work effectively on *data science* problems.

\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]\
\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]\
\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]\
\[embed\]https://medium.com/\@CazoomMaths\_81678/why-is-learning-about-probability-important-d041659fb6bb\[/embed\]

------------------------------------------------------------------------

[*Ankit Rathi*](https://www.ankitrathi.com/) *is an AI architect, published author & well-known speaker. His interest lies primarily in building end-to-end AI applications/products following best practices of Data Engineering and Architecture.*

*Why don’t you connect with Ankit on* [*Twitter*](https://twitter.com/rathiankit)*,* [*LinkedIn*](https://www.linkedin.com/in/ankitrathi/) *or* [*Instagram*](https://instagram.com/ankitrathi/)
