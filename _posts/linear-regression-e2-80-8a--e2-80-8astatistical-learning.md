Title: Linear Regression — Statistical Learning
Date: 2018-08-27 05:27
Author: ankitrathi
Category: Uncategorized
Tags: Data Science, Datadeft, Linear Regression, Machine Learning, Statistical Learning
Slug: linear-regression%e2%80%8a-%e2%80%8astatistical-learning
Status: published

![](https://cdn-images-1.medium.com/max/1200/1*JYeCWrkWtN_iseYlbW79Xw.png)

*This is the 2nd post of blog post series ‘*[*Statistical Learning Notes*](https://medium.com/@rathi.ankit/statistical-learning-notes-series-c8c218102ae0)*’, this post is my notes on ‘Chapter 3 — Linear Regression’ of ‘Introduction to Statistical Learning (ISLR)’, here I have tried to give intuitive understanding of key concepts and how these concepts are connected.*

\[embed\]http://www-bcf.usc.edu/\~gareth/ISL/\[/embed\]

*Note: I suggest the reader to refer ISLR book in case he/she wants to dig further or wants to look for examples.*

------------------------------------------------------------------------

> Visit [ankitrathi.com](http://ankitrathi.com/) now to:

> — to read my blog posts on various topics of AI/ML

> — to keep a tab on latest & relevant news/articles daily from AI/ML world

> — to refer free & useful AI/ML resources

> — to buy my books on discounted price

> — to know more about me and what I am up to these days

**Linear Regression**

Linear regression is a simple approach to supervised learning. It assumes that the dependence of *Y* on *X1;X2; : : :Xp* is linear. True regression functions are never linear, although it may seem *overly simplistic*, linear regression is *extremely useful both conceptually and practically*.

![](https://cdn-images-1.medium.com/max/800/1*9aU2AMo039N6lJKoQFXQug.png)

**Simple Linear Regression**

*Simple linear regression* predicts a quantitative response Y on the basis of a single predictor variable X. It assumes an *approximately linear* relationship between X and Y.

![](https://cdn-images-1.medium.com/max/800/1*txlCLLmAm5-Yip2YLQjN7A.png)

where *β0* and *β1* are two *unknown constants* that represent the *intercept* and *slope*, also known as *coefficients* or *parameters*, and ϵ is the *error* term.

**Estimating Model Coefficients**

Here *β0* and *β1* are typically *unknown*, it is desirable to choose values for *β0* and *β1* such that the resulting line is *as close as possible* to the *observed data points*. The most common method to measure closeness is to minimize the *sum of the residual square (RSS)* differences between the *observed value* and the *predicted value.*

![](https://cdn-images-1.medium.com/max/800/1*SwZcSmYjkB1uzIUPz91lRw.png)

Calculus can be applied to *estimate* the *least squares coefficient estimates* for linear regression to minimize the r*esidual sum of squares* (RSS).

**Assessing Coefficient Estimate Accuracy**

To assess the *coefficient estimate accuracy*, difference between the population regression line and the least squares line can be calculated, which is called *residual standard error* (RSE).

![](https://cdn-images-1.medium.com/max/800/1*JomNJgaZD5NC37QkJMHAzA.png)

Above is the relation between RSE & RSS, where n-2 is the *degree of the freedom* of the observations.

Standard errors can be used to compute *confidence intervals* and *prediction intervals*. A *confidence interval* is defined as a range of values such that there’s a certain likelihood that the range will contain the true unknown value of the parameter.

For simple linear regression the *95% confidence interval* for *β1 & β2* can be approximated by:

![](https://cdn-images-1.medium.com/max/800/1*9NpI_IzzZZUwKmhfQDuk1Q.png)

When predicting an *individual response*, y=f(x)+ϵ, a prediction interval is used. When predicting an *average response*, f(x), a confidence interval is used. Prediction intervals will *always be wider* than confidence intervals because they take into account the uncertainty associated with ϵ, the irreducible error.

The *standard error* can also be used to perform *hypothesis testing* on the estimated coefficients. The most common hypothesis test involves testing:

*Null hypothesis (H0): There is no relationship between X and Y*

*Alternative hypothesis (H1): There is some relationship between X and Y*

Here, the null hypothesis corresponds to testing if *β1=0*, which reduces to which evidences that X is not related to Y. In practice, computing a T-statistic, which measures the number of standard deviations that β1, is away from 0, is useful for determining if an estimate is sufficiently significant to reject the null hypothesis.

![](https://cdn-images-1.medium.com/max/800/1*xiClW1-7RMz0BoMRHl_RGA.png)

If there is no relationship between X and Y, *t-distribution* with n−2 degrees of freedom should be yielded. With such a distribution, it is possible to calculate the probability of observing a value of \|t\| or larger assuming that β1=0. This probability, called the *p-value*, can indicate an *association between the predictor and the response* if sufficiently small.

**Assessing Model Accuracy**

Once the *null hypothesis* has been *rejected*, it may be desirable to quantify *to what extent* the model fits the data. The *quality of a linear regression model* is typically assessed using *residual standard error (RSE)* and the *R² statistic* statistics. The R² statistic is an alternative measure of fit that takes the form of a proportion. The *R² statistic* captures the *proportion of variance* explained as a value between 0 and 1, independent of the unit of Y. The *total sum of squares (TSS*) measures the total variance in the response Y.

![](https://cdn-images-1.medium.com/max/800/1*XfWv0AB3BIu7plA4RMWQ6A.png)

Correlation is another measure of the linear relationship between X and Y. Correlation of can be calculated as:

![](https://cdn-images-1.medium.com/max/800/1*P0wWtlRErgI8xKoXLCIavg.png)

**Multiple Linear Regression**

*Multiple linear regression* extends simple linear regression to accommodate *multiple predictors*.

![](https://cdn-images-1.medium.com/max/800/1*1mI_w2aYYaYuWTOS_NNvuQ.png)

![](https://cdn-images-1.medium.com/max/800/1*d0icRnPHWjHSNXxuoYT5Vg.png)

The *ideal scenario* is when the *predictors are uncorrelated*, correlations amongst predictors cause problems. *Claims of causality* should be avoided for observational data.

**Estimating Multiple Regression Coefficients**

The parameters *β0,β1,…,βp* can be estimated using the same *least squares strategy* as was employed for simple linear regression. Values are chosen for the parameters such that the *residual sum of squares (RSS)* is minimized.

![](https://cdn-images-1.medium.com/max/800/1*Z9TaXFYDAEHL3Uy87Wmoag.png)

**Assessing Multiple Regression Coefficient Accuracy**

In this case,

*Null hypothesis (H0): β1=β2=…=βp=0 &*

*Alternative hypothesis (Ha): at least one of Bj≠0*

The *F-statistic* can be used to determine which hypothesis holds true. The F-statistic can be computed as:

![](https://cdn-images-1.medium.com/max/800/1*bYP97iCz4CnutjuUmUh3Pg.png)

When there is no relationship between the response and the predictors the F-statistic takes on a value close to 1. Conversely, if the alternative hypothesis is true, then the F-statistic will take on a value greater than 1.

When n is large, an F-statistic only slightly greater than 1 may provide evidence against the null hypothesis. If n is small, a large F-statistic is needed to reject the null hypothesis. The F-statistic works best when p is relatively small or when p is relatively small compared to n.

**Selecting Important Variables**

Now we know that *at least one of the predictors* is associated with the response, but *which* of the predictors are related to the response? The process of *variable selection* would involve testing many different models but there are a total of *2\^p models* that contain subsets of p predictors.

*Forward selection* begins with a *null model* and attempts p simple linear regressions, keeping whichever predictor results in the *lowest RSS*.

*Backward selection* starts with all variables in the model and keep removing variables with *largest p-values.*

*Mixed selection* begins with a null model, repeatedly adding whichever predictor yields the best fit. As more predictors are added, variables with *p-values of a certain threshold* are removed from the model.

**Assessing Multiple Regression Model Fit**

In multiple linear regression, R² is equal to the square of the correlation between the response and the fitted linear model. R² will always increase when more variables are added to the model, even when those variables are only weakly related to the response.

Residual standard error (RSE) can also be used to assess the fit of a multiple linear regression model.

![](https://cdn-images-1.medium.com/max/800/1*zvv_G0zyvXpVIr0Q7JUd8Q.png)

**Qualitative Predictors**

When a qualitative predictor or factor has only two possible values or levels, it can be incorporated into the model by introducing an indicator variable or dummy variable that takes on only two numerical values.

![](https://cdn-images-1.medium.com/max/800/1*3EVGCAxNlQG8S5t-XNs5yA.png)

When a qualitative predictor takes on more than two values, multiple dummy variables can be used.

![](https://cdn-images-1.medium.com/max/800/1*mSHLm_7bodvmhyGYRIAs-g.png)

**Extending the Linear Model**

Though linear regression provides interpretable results, it makes several highly restrictive assumptions that are often violated in practice.

First assumption: the relationship between the predictors and the response is *additive,* which implies that the effect of changes in a predictor Xj on the response Y is independent of the values of the other predictors.

Second assumption: the relationship between the predictors and the response is *linear* which implies that the change in the response Y due to a one-unit change in Xj is constant regardless of the value of Xj.

**Modeling Predictor Interaction**

Predictor interaction is the increase in effectiveness of a predictor given an increase in another predictor and vice-versa. The *hierarchical principle* says ‘when an *interaction term* is included in the model, the *main effects* should also be included, *even if* the *p-values associated* with their coefficients *are not significant*’.

**Modeling Non-Linear Relationships**

To mitigate the effects of the *linear assumption* it is possible to accommodate non-linear relationships by *incorporating polynomial functions* of the predictors in the regression model.

![](https://cdn-images-1.medium.com/max/800/1*ig3SQ_xv6NQQZFEt_Bg_7Q.png)

![](https://cdn-images-1.medium.com/max/800/1*YvanoNbFRECMUmlvLs7F9Q.png)

**Common Problems with Linear Regression**

*1. Non-linearity of the response-predictor relationships*

If the true relationship between the response and predictors is *far from linear*, then virtually all conclusions that can be drawn from the model are suspect and prediction accuracy can be significantly reduced. *Residual plots* are a useful graphical tool for *identifying non-linearity*.

*2. Correlation of error terms*

An important assumption of linear regression is that the error terms, *ϵ1,ϵ2,…,ϵn*, are uncorrelated. Correlated error terms can make a model appear to be stronger than it really is.

*3. Non-constant variance of error terms*

Linear regression also assumes that the error terms have a constant variance. Standard errors, confidence intervals, and hypothesis testing all depend on this assumption. One way to address this problem is to transform the response Y.

*4. Outliers*

An outlier is a point for which actual point is far from the value predicted by the model. Excluding outliers can result in improved residual standard error (RSE) and improved R² values, usually with negligible impact to the least squares fit but outliers should be *removed with caution* as it may indicate a *missing predictor* or *other deficiency* in the model.

*5. High-leverage points*

Observations with *high leverage* are those that have an *unusual value* for the predictor for the given response. High leverage observations tend to have a sizable impact on the estimated regression line and as a result, removing them can yield improvements in model fit.

*6. Collinearity*

*Collinearity* refers to the situation in which *two or more predictor* variables are *closely related* to one another. It can pose *problems for linear regression* because it can make it hard to determine the *individual impact* of collinear predictors on the response. A way to detect collinearity is to generate a *correlation matrix* of the predictors.

*Multicollinearity* is the *collinearity* which exists between *three or more variables* even if no pair of variables have high correlation. Multicollinearity can be detected by computing the *variance inflation factor* (VIF).

![](https://cdn-images-1.medium.com/max/800/1*GO9iwELo1DIACJQ_tzXm-w.png)

One way to handle collinearity is to *drop one of the problematic variables*. Another way of handling collinearity is to *combine the collinear predictors together* into a single predictor by some kind of transformation such as an average.

**Parametric Methods Versus Non-Parametric Methods**

A *non-parametric method* akin to linear regression is *k-nearest neighbors regression* which is closely related to the k-nearest neighbors classifier.

A parametric approach will *outperform* a non-parametric approach if the parametric form is close to the *true form* of f(X). The choice of a parametric approach versus a non-parametric approach will depend largely on the *bias-variance trade-off* and the *shape of the function f(X)*.

In *higher dimensions*, K-nearest neighbors regression often performs worse than linear regression, which is often called the *curse of dimensionality*. As a general rule, *parametric models will tend to outperform non-parametric models* when there are only a *small number of observations per predictor*.

**References:**

\[embed\]http://www-bcf.usc.edu/\~gareth/ISL/\[/embed\]\
<https://lagunita.stanford.edu/c4x/HumanitiesScience/StatLearning/asset/linear_regression.pdf>

------------------------------------------------------------------------

*Thank you for reading my post. If you enjoyed it, please clap button* 👏 *so others might stumble upon it. I regularly write about Data & Technology on* [*LinkedIn*](https://www.linkedin.com/today/posts/ankitrathi) *&* [*Medium*](https://medium.com/@rathi.ankit)*. If you would like to read my future posts then simply ‘Connect’ or ‘Follow’. Also feel free to listen to me on* [*SoundCloud*](https://soundcloud.com/ankitrathi)*.*
