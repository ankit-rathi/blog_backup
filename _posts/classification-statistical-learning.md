Title: Classification — Statistical Learning
Date: 2018-08-29 14:46
Author: ankitrathi
Category: Uncategorized
Tags: Classification, Data Science, Datadeft, Logistic Regression, Machine Learning
Slug: classification-statistical-learning
Status: published

![](https://cdn-images-1.medium.com/max/1200/1*WE7ndSyOB2lTp4e9OVD5RA.png)

*This is the 3rd post of blog post series ‘*[*Statistical Learning Notes*](https://medium.com/@rathi.ankit/statistical-learning-notes-series-c8c218102ae0)*’, this post is my notes on ‘Chapter 4 — Classification’ of ‘Introduction to Statistical Learning (ISLR)’. Here I have tried to give an intuitive understanding of key concepts and how these concepts are related to Classification.*

\[embed\]http://www-bcf.usc.edu/\~gareth/ISL/\[/embed\]

*Note: I suggest the reader to refer ISLR book in case he/she wants to dig further or wants to look for examples.*

------------------------------------------------------------------------

Predicting a *qualitative response* for an observation can be referred to as *classifying* that observation, since it involves *assigning* the observation to a *category* or *class*.

Given a feature vector X and a qualitative response Y taking values in the set *C*, the classification task is to build a function C(X) that takes as input the feature vector X and predicts its value for Y. Often we are more interested in *estimating the probabilities* that X belongs to *each category* in *C*.

![](https://cdn-images-1.medium.com/max/800/1*McStH0zjIgyg6N2O5uQUhg.png)

We might think that *regression* is perfect for *classification* task as well. However, linear regression might produce *probabilities* *less than zero* or *bigger than one*. Logistic regression is more appropriate.

![](https://cdn-images-1.medium.com/max/800/1*bLw4dtlQGDsnhMOkOH534g.png)

Now suppose we have a *response variable* with *three* possible values. If we *code the categories*, it will suggest an ordering, and in fact implies that the *difference between categories* is the same. So, we can see that *Linear Regression* is not appropriate here. *Multi-class Logistic Regression* or *Discriminant Analysis* are more appropriate.

**Logistic Regression**

*Logistic regression* models the *probability* that y belongs to a particular category rather than modeling the response itself. It uses the *logistic function* to ensure a prediction between 0 and 1. The logistic function takes the form:

![](https://cdn-images-1.medium.com/max/800/1*JXY8s-7rc9M_QD47iuuTmw.png)

**Estimating Regression Coefficients**

*Logistic regression* uses a strategy called *maximum likelihood* to estimate regression coefficients.

We use maximum likelihood to estimate the parameters.

![](https://cdn-images-1.medium.com/max/800/1*fqC_j-VdT4upIQ-gRMha-w.png)

This *likelihood* gives the probability of the observed 0s and 1s in the data. We pick 0 and 1 to maximize the likelihood of the observed data.

Logistic regression measures the accuracy of coefficient estimates using a quantity called the *z-statistic*. The z-statistic is similar to the *t-statistic*. The *z-statistic* for *β1* is represented by:

![](https://cdn-images-1.medium.com/max/800/1*F3lg10fXNDkvZp7w56AgkA.png)

A *large z-statistic* offers *evidence against* the *null hypothesis*.

In logistic regression, the null hypothesis:

Null hypothesis (*H0*): *β1=0* implies that

![](https://cdn-images-1.medium.com/max/800/1*x9_O-tXN7fzB46GPMqOC9g.png)

which means *p(X)* does not depend on *X*.

**Making Predictions**

Once coefficients have been estimated, *predictions* can be made by plugging the coefficients into the *model equation*.

In general, the *estimated intercept* (*β0*) is of limited interest since it mainly captures the *ratio* of *positive* and *negative* classifications in the given data set.

Similar to linear regression, *dummy variables* can be used to accommodate *qualitative predictors*.

**Multiple Logistic Regression**

Using a strategy similar to that employed for linear regression, *multiple logistic regression* can be generalized as:

![](https://cdn-images-1.medium.com/max/800/1*LHkrh4jd2HDHtew5m8jEag.png)

*Maximum likelihood* is also used to estimate *β0,β1,…,βp* in the case of multiple logistic regression.

In general, the scenario in which the result obtained with a single predictor does not match the result with multiple predictors, especially when there is correlation among the predictors, is referred to as *confounding*. More specifically, *confounding* describes situations in which the *experimental controls* do not adequately allow for ruling out *alternative explanations* for the observed relationship between the predictors and the response.

**Logistic Regression For More Than Two Classes**

Though multi-class logistic regression is possible, *discriminant analysis* tends to be the preferred means of handling multi-class classification.

**Linear Discriminant Analysis (LDA)**

While *logistic regression* models the *conditional distribution* of the response Y given the predictor(s) X, *linear discriminant analysis* (LDA) is an approach to model the *distribution* of X in each of the *classes separately*, and then use *Bayes’ theorem* to flip things around and obtain *Pr(Y/X)*.

*Linear discriminant analysis* is popular when there are *more than two response* classes, because it also provides *low-dimensional views* of the data. Beyond its popularity, linear discriminant analysis also benefits from not being susceptible to some of the problems that logistic regression suffers from:

-   The *parameter estimates* for logistic regression can be *surprisingly unstable* when the *response classes are well separated*. Linear discriminant analysis does not suffer from this problem.
-   *Logistic regression* is *more unstable* than *linear discriminant analysis* when *n is small* and the *distribution* of the predictors X is *approximately normal* in each of the response classes.

When we use *normal (Gaussian) distributions* for each class, this leads to *linear or quadratic discriminant analysis*. However, this approach is quite general, and other distributions can be used as well.

**Classification With Bayes’ Theorem**

Assuming a qualitative variable YY that can take on K≥2 distinct, unordered values, the *prior probability* describes the probability that a given observation is associated with the *kth* class of the response variable Y.

The *density function* of X for an observation that comes from the *kth* class is defined as:

![](https://cdn-images-1.medium.com/max/800/1*qU7XHSk5R_uYSAC0WfTd1g.png)

This means that *fk(X)* should be *relatively large* if there’s a *high probability* that an observation from the *kth* class features X=x. Conversely, *fk(X)* will be *relatively small* if it is unlikely that an observation in class k would feature X=x.

Following this intuition, *Bayes’ theorem* states:

![](https://cdn-images-1.medium.com/max/800/1*Dv0fY6GfoWq1YmUceSBIlw.png)

where *πk* denotes the *prior probability* that the chosen observation comes from the *kth* class. This equation is sometimes abbreviated as *pk(x)*.

*pk(x)=Pr(Y=k\|X)* is also known as the *posterior probability*, or the probability that an observation belongs to the *kth* class, given the predictor value for that observation.

![](https://cdn-images-1.medium.com/max/800/1*war7jDX-ccPt-ip09kAA0Q.png)

Estimating the *prior probability* (*πk*) is easy given a random sample of responses from the population.

Estimating the *density function fk(X)* tends to be harder, but making some assumptions about the form of the densities can simplify things. A good estimate for *fk(X)* allows for developing a classifier that approximates the Bayes’ classifier which has the *lowest possible error rate* since it always selects the class for which *pk(x)* is largest.

**Linear Discriminant Analysis For One Predictor**

When only considering one predictor, if we assume that fk(X)fk(X) has a *normal or Gaussian distribution*, the normal density is described by:

![](https://cdn-images-1.medium.com/max/800/1*fODhv6dp0ujSn2EnRHuLgg.png)

where *μk* is the *mean parameter* for the *kth* class and *σ²k* is the *variable parameter* for the *kth class*.

The *density function* can be further simplified by assuming that the *variance* *terms*, *σ²1,…,σ²k*, are all equal in which case the variance is denoted by σ².

Plugging the simplified normal density function into *Bayes’ theorem* yields:

![](https://cdn-images-1.medium.com/max/800/1*3JNK-NntqmlgI8tlAZkA6g.png)

It can be shown that by taking a log of both sides and removing terms that are not class specific, a simpler equation can be extracted:

![](https://cdn-images-1.medium.com/max/800/1*NJ38XF-ReqaTvbXXYGCoYQ.png)

Using above equation, an observation can be classified by taking the class yields the largest value.

Linear discriminant analysis uses the following estimated values for μ\^k and σ²:

![](https://cdn-images-1.medium.com/max/800/1*4ySexeFyqgCvC-NKGNWfRw.png)

where n is the total number of training observations and *nk* is the number of training observations in class k. The estimate of *μ\^k* is the average value of x for all training observations in class k. The estimate of σ² can be seen as a weighted average of the sample variance for all k classes.

When the class prior probabilities, *π1,…,πk,*is not known, it can be estimated using the proportion of training observations that fall into the *kth* class:

*πk*=*nk/n*

Plugging the estimates for *μ\^k* and *σ²k* into the modified Bayes’ theorem yields the *linear discriminant analysis classifier*:

![](https://cdn-images-1.medium.com/max/800/1*4Xf-yf2oqIWMU6VxibjWRw.png)

which assigns an observation *X=x* to whichever class yields the largest value.

This classifier is described as linear because the discriminant function *δ\^k(x)* is linear in terms of *x* and not a more complex function.

The *linear discriminant analysis classifier* assumes that the observations from *each class follow a normal distribution* with a class specific average vector and constant variance (σ²), and uses these simplifications to build a Bayes’ theorem based classifier.

**Linear Discriminant Analysis with Multiple Predictors**

*Multivariate linear discriminant analysis* assumes that *X=(X1,X2,…,Xp)* comes from a *multivariate normal distribution* with a *class-specific mean vector* and a *common covariance matrix*.

The *multivariate Gaussian distribution* used by *linear discriminant analysis* assumes that each predictor follows a *one-dimensional normal distribution* with *some correlation* between the predictors. The *more correlation* between predictors, the *more* the bell shape of the normal distribution will be *distorted*.

A p-dimensional variable X can be indicated to have a multivariate Gaussian distribution with the notation X∼N(μ,Σ) where E(x)=μ is the mean of XX (a vector with p components) and Cov(X)=Σ is the p x p covariance matrix of X.

As was the case for one-dimensional linear discriminant analysis, it is necessary to estimate the unknown parameters μ1,…,μk, π1,…,πk, and Σ. The formulas used in the multi-dimensional case are similar to those used with just a single dimension.

Since, even in the multivariate case, the *linear discriminant analysis* decision rule *relates to X in a linear fashion*, the name linear discriminant analysis holds. And as with other methods, the *higher the ratio of parameters* p, to number of samples n, the *more likely overfitting* will occur.

In general, binary classifiers are subject to two kinds of error: *false positives* and *false negatives*. A *confusion matrix* can be a useful way to display these error rates. *Class-specific performance* is also important to consider because in some cases a particular class will contain the *bulk of the error*.

The term *sensitivity* refers to the percentage of observations correctly positively classified (true positives) and *specificity* refers to the percentage of observations correctly negatively classified (true negatives).

A *ROC curve* is a useful graphic for displaying the two types of error rates for all possible thresholds. ROC is a historic acronym that comes from communications theory and stands for *receiver operating characteristics*.

![](https://cdn-images-1.medium.com/max/800/0*Gg3ixBvG35uHg-Th.jpg)

The *overall performance* of a classifier summarized over all possible thresholds is quantified by the *area under the ROC curve*.

A more ideal ROC curve will hold more tightly to the top left corner which, in turn, will increase the area under the ROC curve. A classifier that performs no better than chance will have an area under the ROC curve less than or equal to 0.5 when evaluated against a test data set.

In summary, varying the *classifier threshold* changes its *true positive* and *false positive* rate, also called *sensitivity* and (*1−specificity*).

**Quadratic Discriminant Analysis**

*Quadratic discriminant analysis* offers an *alternative approach* to linear discriminant analysis that makes most of the same assumptions, except that quadratic discriminant analysis assumes that *each class* has its own *covariance matrix*.

The quadratic discriminant analysis Bayes classifier gets its name from the fact that it is a *quadratic function* in terms *of x*.

The choice between a *shared covariance matrix* (like that assumed in *linear discriminant analysis*) and a *class-specific covariance matrix* (like that assumed in *quadratic discriminant analysis*) amounts to a *bias-variance trade-off*.

**Comparing Classification Methods**

Since *logistic regression* and *linear discriminant analysis* are both linear in terms of *x*,the *primary difference* between the two methods is *their fitting procedures*. Linear discriminant analysis assumes that observations come from a *Gaussian distribution* with a *common covariance matrix*, and as such, out performs logistic regression in cases where these assumptions hold true.

*K-nearest neighbors* can outperform *logistics regression* and *linear discriminant analysis* when the *decision boundary* is *highly non-linear*, but *at the cost of* a *less interpretable model*.

*Quadratic discriminant analysis* falls somewhere between the linear approaches of *linear discriminant analysis* and *logistic regression* and the non-parametric approach of *K-nearest neighbors*. Since quadratic linear analysis models a *quadratic decision boundary*, it has more capacity for modeling a wider range of problems. *Quadratic discriminant analysis* is not as flexible as *K-nearest neighbors*, however it can perform better than *K-nearest neighbors* when there are *fewer training observations* due to its high bias.

*Linear discriminant analysis* and *logistic regression* will perform well when the true *decision boundary* is *linear*. *Quadratic discriminant analysis* may give *better results* when the *decision boundary* is *moderately non-linear*. *Non-parametric* approaches like *K-nearest neighbors* may give better results when the *decision boundary* is *more complex* and the right level of smoothing is employed.

As was the case in the *regression* setting, it is possible to apply *non-linear transformations* to the predictors to better accommodate non-linear relationships between the response and the predictors. The effectiveness of this approach will depend on whether or not the *increase in variance* introduced by the *increase in flexibility* is offset by the *reduction in bias*.

It is possible to add *quadratic terms* and *cross products* to the *linear discriminant analysis* model such that it has the same form as *quadratic discriminant analysis*, however the *parameter estimates* for each of the models would be *different*. In this fashion, it’s possible to build a model that falls somewhere between *linear discriminant analysis* and *quadratic discriminant analysis*.

**References:**

\[embed\]http://www-bcf.usc.edu/\~gareth/ISL/\[/embed\]\
<https://lagunita.stanford.edu/c4x/HumanitiesScience/StatLearning/asset/classification.pdf>

------------------------------------------------------------------------

*Thank you for reading my post. I regularly write about Data & Technology on* [*LinkedIn*](https://www.linkedin.com/today/posts/ankitrathi) *&* [*Medium*](https://medium.com/@rathi.ankit)*. If you would like to read my future posts then simply ‘Connect’ or ‘Follow’. Also feel free to listen to me on* [*SoundCloud*](https://soundcloud.com/ankitrathi)*.*
