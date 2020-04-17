Title: Inferential Statistics for Data Science
Date: 2018-08-07 13:21
Author: ankitrathi
Category: Uncategorized
Tags: Data Science, Inferential Statistics, Machine Learning, Probability, Statistics
Slug: inferential-statistics-for-data-science
Status: published

![Inferential Statistics for Data Science](https://cdn-images-1.medium.com/max/1200/1*r4-qlit-FoQkka5ThRTG8Q.png)

*This is the 4th post of blog post series ‘*[*Probability & Statistics for Data Science*](https://www.ankitrathi.com/post/probability-statistics-for-data-science-series)*’, this post covers these topics related to inferential statistics and their significance in data science.*

-   *Inferential Statistics*
-   *Sampling Distributions & Estimation*
-   *Hypothesis Testing (One and Two Group Means)*
-   *Hypothesis Testing (Categorical Data)*
-   *Hypothesis Testing (More Than Two Group Means)*
-   *Quantitative Data (Correlation & Regression)*
-   *Significance in Data Science*

------------------------------------------------------------------------

> Visit [ankitrathi.com](http://ankitrathi.com/) now to:

> — to read my blog posts on various topics of AI/ML

> — to keep a tab on latest & relevant news/articles daily from AI/ML world

> — to refer free & useful AI/ML resources

> — to buy my books on discounted price

> — to know more about me and what I am up to these days

**Inferential Statistics**

*Inferential statistics* allows you to make inferences about the *population* from the *sample* data.

![](https://cdn-images-1.medium.com/max/800/0*o0NliEWAfYeZ0WHZ.jpg)

**Population & Sample**

A *sample* is a representative subset of a *population*. Conducting a census on population is an ideal but impractical approach in most of the cases. *Sampling* is much more practical, however it is prone to *sampling error.* A sample non-representative of population is called *bias,* method chosen for such sampling is called *sampling bias. Convenience bias*, *judgement bias*, *size bias*, *response bias* are main types of sampling bias. The best technique for reducing bias in sampling is *randomization*. *Simple random sampling* is the simplest of randomization techniques, *cluster sampling* & *stratified sampling* are other systematic sampling techniques.

**Sampling Distributions**

*Sample means* become more and more *normally distributed* around the true mean (the population parameter) as we increase our *sample size*. The *variability* of the sample means *decreases* as *sample size increases*.

**Central Limit Theorem**

The *Central Limit Theorem* is used to help us understand the following facts regardless of whether the population distribution is normal or not:\
1. the *mean* of the sample means is the same as the population mean\
2. the *standard deviation* of the sample means is always equal to the *standard error*.\
3. the *distribution* of *sample means* will become increasingly more *normal* as the sample size increases.

**Confidence Intervals**

A *sample mean* can be referred to as a *point estimate* of a *population mean*. A *confidence interval* is always centered around the mean of your sample. To construct the interval, you add a *margin of error*. The *margin of error* is found by multiplying the *standard error* of the mean by the *z-score* of the percent confidence level:

![](https://cdn-images-1.medium.com/max/800/0*Z4U1QpANvOLMKF0b.png)

![](https://cdn-images-1.medium.com/max/800/0*fAdTwLXc7S3X44CW.jpg)

The *confidence level* indicates the number of times out of 100 that the mean of the population will be within the given interval of the sample mean.

**Hypothesis Testing**

Hypothesis testing is a kind of *statistical inference* that involves asking a question, collecting data, and then examining what the data tells us about how to proceed. The hypothesis to be tested is called the *null hypothesis* and given the symbol Ho. We test the null hypothesis against an *alternative hypothesis*, which is given the symbol Ha.

![](https://cdn-images-1.medium.com/max/800/1*4c72kKs77I7nJmGtYq3dkw.png)

When a *hypothesis* is tested, we must decide on how much of a difference between means is necessary in order to reject the null hypothesis. Statisticians first choose a *level of significance* or *alpha(α) level* for their hypothesis test.

![](https://cdn-images-1.medium.com/max/800/1*AkhRx0c5ROtVQaFexaUhSQ.png)

*Critical values* are the values that indicate the edge of the critical region. *Critical regions* describe the entire area of values that indicate you *reject the null hypothesis*.

![left, right & two-tailed tests](https://cdn-images-1.medium.com/max/800/1*577q2zOtWH488sXKom-88w.png)

These are the *four basic steps* we follow for (one & two group means) hypothesis testing:

1.  State the *null* and *alternative* hypotheses.
2.  Select the *appropriate significance level* and check the *test assumptions*.
3.  Analyze the data and compute the *test statistic*.
4.  Interpret the *result*.

**Hypothesis Testing (One and Two Group Means)**

**Hypothesis Test on One Sample Mean When the Population Parameters are Known**

We find the *z-statistic* of our sample mean in the *sampling distribution* and determine if that *z-score* falls within the *critical(rejection) region* or not. This test is *only appropriate when* you know the *true mean* and *standard deviation* of the *population*.

![](https://cdn-images-1.medium.com/max/800/1*K8QeUa6X28OXashLRNidRQ.png)

**Hypothesis Tests When You Don’t Know Your Population Parameters**

The *Student’s t-distribution* is similar to the normal distribution, except it is more spread out and wider in appearance, and has thicker tails. The differences between the *t-distribution* and the *normal distribution* are more exaggerated when there are fewer data points, and therefore *fewer degrees of freedom*.

![](https://cdn-images-1.medium.com/max/800/1*LlBltIwkHXx6CgncSB_Oiw.png)

![](https://cdn-images-1.medium.com/max/800/1*fMUfx6aKyMdbUPjdt730Lg.png)

**Estimation as a follow-up to a Hypothesis Test**

When a *hypothesis is rejected*, it is often useful to turn to estimation to try to capture the *true value* of the *population mean*.

**Two-Sample T Tests**

**Independent Vs Dependent Samples**

When we have *independent samples* we assume that the scores of one sample *do not affect* the other.

![unpaired t-test](https://cdn-images-1.medium.com/max/800/1*w-YboTzRz6BJXp3vCgVwLg.png)

In two *dependent samples* of data, each score in one sample *is paired with* a specific score in the other sample.

![paired t-test](https://cdn-images-1.medium.com/max/800/1*FV3K60xleq89RiP9LINVfg.png)

**Hypothesis Testing (Categorical Data)**

*Chi-square test* is used for *categorical data* and it can be used to estimate how closely the distribution of a categorical variable matches an expected distribution (the *goodness-of-fit* test), or to estimate whether two categorical variables are independent of one another (the *test of independence*).

![*goodness-of-fit*](https://cdn-images-1.medium.com/max/800/1*Ah06mmtq_lVz3sI3GrQnKg.png)

*degree of freedom (d f) = no. of categories(c)−1*

![test of independence](https://cdn-images-1.medium.com/max/800/1*kcxjdwaReZtIjQDq8lRdEQ.png)

*degree of freedom (df) = (rows−1)(columns−1)*

**Hypothesis Testing (More Than Two Group Means)**

*Analysis of Variance (ANOVA)* allows us to test the hypothesis that *multiple population means and variances* of scores are *equal*. We can conduct a series of t-tests instead of ANOVA but that would be tedious due to various factors.

We follow a series of steps to perform ANOVA:

1.  Calculate the *total sum of squares* (SST )
2.  Calculate the *sum of squares between* (SSB)
3.  Find the *sum of squares within groups* (SSW ) by subtracting
4.  Next solve for *degrees of freedom* for the test
5.  Using the values, you can now calculate the *Mean Squares Between* (MSB) and *Mean Squares Within* (MSW ) using the relationships below
6.  Finally, calculate the *F statistic* using the following ratio
7.  It is easy to fill in the Table from here — and also to see that once the SS and df are filled in, the remaining values in the table for MS and F are simple calculations
8.  Find *F critical*

![ANOVA formulaes](https://cdn-images-1.medium.com/max/800/1*FzYvawbu_K4irFgTbO_o3Q.png)

If *F-value* from the ANOVA test is greater than the *F-critical value*, so we would reject our Null Hypothesis.

**One-Way ANOVA**

*One-way ANOVA* method is the procedure for testing the null hypothesis that the population means and variances of *a single independent variable* are equal.

**Two-Way ANOVA**

*Two-way ANOVA* method is the procedure for testing the null hypothesis that the *population means and variances* of *two independent variables* are equal. With this method, we are *not only* able to study the *effect of two independent variables*, but also the *interaction between these variables*.

We can also do two separate one-way ANOVA but two-way ANOVA gives us *Efficiency, Control & Interaction*.

**Quantitative Data (Correlation & Regression)**

**Correlation**

*Correlation* refers to a *mutual relationship* or *association* between quantitative variables. It can help in predicting one quantity from another. It *often* indicates the *presence of a causal relationship*. It used as a basic quantity and *foundation* for many other *modeling techniques*.

![Pearson Correlation](https://cdn-images-1.medium.com/max/800/1*uf1MiJerVbP2uAdlfAJLpw.png)

![](https://cdn-images-1.medium.com/max/800/0*87dwGgWPM3MVUHHl)

**Regression**

*Regression* analysis is a *set of statistical processes* for *estimating the relationships* among variables.

![Regression](https://cdn-images-1.medium.com/max/800/0*CNxCQXwpdNs0MNvN.png)

**Simple Regression**

This method uses a *single independent variable* to predict a dependent variable *by fitting* the best relationship.

![](https://cdn-images-1.medium.com/max/800/1*csk8XTXy0j__hm_kbkwxCw.jpeg)

**Multiple Regression**

This method uses *more than one independent variable* to predict a dependent variable *by fitting* the best relationship.

![](https://cdn-images-1.medium.com/max/800/1*DaFQEFYBNVCoVMNEB9KOGg.jpeg)

It works best when *multicollinearity* is absent. It’s a phenomenon in which two or more predictor variables are *highly correlated*.

**Nonlinear Regression**

In this method, observational data are modeled by a function which is a *nonlinear combination* of the model parameters and depends on *one or more independent variables*.

![](https://cdn-images-1.medium.com/max/800/0*ZdPVRLHappcGzGEy)

**Significance in Data Science**

In *data science*, *inferential statistics* is used is many ways:

-   Making *inferences* about the *population* from the *sample*.
-   Concluding whether a sample is *significantly different* from the population.
-   If *adding or removing a feature* from a model will really help to improve the model.
-   If one *model is significantly better* than the other?
-   *Hypothesis testing* in general.

**References:**

\[embed\]https://classroom.udacity.com/courses/ud201\[/embed\]\
\[embed\]https://classroom.udacity.com/courses/ud201\[/embed\]

------------------------------------------------------------------------

[*Ankit Rathi*](https://www.ankitrathi.com/) *is an AI architect, published author & well-known speaker. His interest lies primarily in building end-to-end AI applications/products following best practices of Data Engineering and Architecture.*

*Why don’t you connect with Ankit on* [*Twitter*](https://twitter.com/rathiankit)*,* [*LinkedIn*](https://www.linkedin.com/in/ankitrathi/) *or* [*Instagram*](https://instagram.com/ankitrathi/)
