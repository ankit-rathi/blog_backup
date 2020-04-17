Title: Resampling Methods — Statistical Learning
Date: 2018-09-05 09:58
Author: ankitrathi
Category: Uncategorized
Tags: Data Science, Datadeft, Machine Learning, Statistical Learning, Statistics
Slug: resampling-methods-statistical-learning
Status: published

![](https://cdn-images-1.medium.com/max/1200/1*__sUH96lwPg_ERWDFWAwnA.png)

*This is the 4th post of the blog post series ‘*[*Statistical Learning Notes*](https://medium.com/@rathi.ankit/statistical-learning-notes-series-c8c218102ae0)*’. This post is my notes on ‘Chapter 5— Resampling Methods’ of ‘Introduction to Statistical Learning (ISLR)’, here I have tried to give an intuitive understanding of key concepts and how these concepts are connected to Resampling.*

\[embed\]http://www-bcf.usc.edu/\~gareth/ISL/\[/embed\]

*Note: I suggest the reader to refer to the ISLR book in case he/she wants to dig further or wants to look for examples.*

------------------------------------------------------------------------

*Resampling methods* are processes of *repeatedly drawing samples* from a data set and *refitting a given model* on each sample with the *goal of learning more* about the fitted model. *Resampling methods* can be expensive since they require repeatedly performing the *same statistical methods* on *N different subsets* of the data.

*Resampling methods* refit a *model of interest* to samples formed from the training set, in order to obtain additional information about the fitted model. For example, they provide *estimates of test-set prediction error*, and the *standard deviation* and *bias* of our parameter estimates.

The *test error* is the *average error* that results from using a *statistical learning method* to predict the response on a new observation, one that was not used in training the method. In contrast, the *training error* can be *easily calculated* by applying the *statistical learning method* to the observations used in its training.

![](https://cdn-images-1.medium.com/max/800/1*-nIi8cVzCfxSalmbAsGDTw.png)

But the *training error rate* often is *quite different* from the *test error rate*, and in particular the former can *dramatically underestimate* the latter.

*Cross validation* is a *resampling method* that can be used to estimate a given statistical methods *test error* or to determine the appropriate amount of *flexibility*. *Model assessment* is the process of evaluating a *model’s performance*. *Model selection* is the process of selecting the *appropriate level of flexibility* for a model. *Bootstrap* is used in a number of contexts, but *most commonly* it is used to provide *a measure of accuracy* of a given *statistical learning method* or *parameter estimate*.

**Cross Validation**

In the *absence* of a *large test set* that can be used to determine the *test error rate*, there are a *number of techniques* that can be used to *estimate the error rate* using training data.

The *validation set* approach involves *randomly dividing* the available observations into two groups, a training set and a *validation* or *hold-out* set. The model is then fit using the training set and then the fitted model is used to predict responses for the observations in the validation set.

![](https://cdn-images-1.medium.com/max/800/1*bAEW6gdHqAm9SEeslISeLA.png)

The resulting *validation set error rate* offers an *estimate* of the *test error rate*.

Though conceptually simple and easy to implement, the *validation set approach* has *two potential drawbacks*.

1.  The estimated test error rate can be *highly variable* depending on which observations fall into the training set and which observations fall into the test/validation set.
2.  The estimated error rate tends to be *overestimated* since the given statistical method was trained with fewer observations than it would have if fewer observations had been set aside for validation.

Cross-validation is a *refinement* of the validation set approach that mitigates these two issues.

**Leave-one-out Cross Validation (LOOCV)**

*Leave-one-out cross-validation* (LOOCV) is closely related to the *validation set* approach, but it attempts to address that method’s drawbacks.

![](https://cdn-images-1.medium.com/max/800/1*ZxGuHLt0qGLbpZBXxo4Qsg.png)

Leave-one-out cross-validation *withholds* only a *single observation* for the validation set. This process can be repeated *n* times with each observation being withheld once. This yields *n* *mean squared errors* which can be averaged together to yield the leave-one-out cross-validation *estimate of the test mean squared error*.

![](https://cdn-images-1.medium.com/max/800/1*VYREzlfNLPkMfXClss7TEg.png)

*Leave-one-out cross validation* has much *less bias* than the validation set approach. Leave-one-out cross validation also *tends not to overestimate* the test mean squared error since many more observations are used for training. In addition, leave-one-out cross validation is *much less variable*, in fact, it always yields the same result since there’s *no randomness* in the set splits.

Leave-one-out cross validation can be *expensive to implement* since the model has to be fit n times. This can be especially expensive in situations where n is very large and/or when each individual model is slow to fit.

Leave-one-out cross validation is a very *good general method* which can be used with logistic regression, linear discriminant analysis, and many other methods. That said, the shortcutting method doesn’t hold in general which means the model generally needs to be refit *n* times.

**K-Fold Cross Validation**

*K-fold cross validation* operates by randomly dividing the set of observations into *K groups or folds* of roughly equal size. Similar to leave-one-out cross validation, each of the *K folds* is used as the *validation set* while the other K−1 folds are used as the test set to generate K estimates of the test error. The K-fold cross validation estimated test error comes from the average of these estimates.

![](https://cdn-images-1.medium.com/max/800/1*uj5bBrYbVSqXBma7GgbLdQ.png)

It can be shown that leave-one-out cross validation is a special case of K-fold cross validation where *K=n*.

Typical values for K are 5 or 10 since these values *require less computation* than when K is equal to n.

Cross validation can be used both to estimate how well a given statistical learning procedure might perform on new data and to *estimate the minimum point* in the estimated test mean squared error curve, which can be useful when *comparing statistical learning methods* or when *comparing different levels of flexibility* for a single statistical learning method.

![](https://cdn-images-1.medium.com/max/800/1*ozvgGozsJzee8IPuSTUh2g.png)

**Bias-Variance Trade-Off for K-Fold Cross Validation**

There is a *bias-variance trade-off* inherent to the *choice of K* in K-fold cross validation. Typically, values of *K=5* or *K=10* are used as these values have been empirically shown to produce test error rate estimates that suffer from *neither excessively high bias nor very high variance*.

In terms of *bias*, *leave-one-out cross validation is preferable* to K-fold cross validation and K-fold cross validation is preferable to the validation set approach.

In terms of *variance*, *K-fold cross validation where K\<n is preferable* to leave-one-out cross validation and leave-one-out cross validation is preferable to the validation set approach.

**The Bootstrap**

The *bootstrap* is a widely applicable tool that can be used to *quantify the uncertainty* associated with a given *estimator or statistical learning approach*, including those for which it is difficult to obtain a *measure of variability*.

The *bootstrap* generates distinct data sets by *repeatedly sampling* observations from the original data set. These generated data sets can be used to *estimate variability* in lieu of sampling independent data sets from the full population.

![](https://cdn-images-1.medium.com/max/800/0*sAoa2xdY9twgTSZz.png)

The sampling employed by the *bootstrap* involves randomly selecting *n* observations with replacement, which means some observations can be selected multiple times while other observations are not included at all.

This process is repeated *B* times to yield *B* bootstrap data sets, *Z∗1,Z∗2,…,Z∗B*,which can be used to *estimate* other quantities such as *standard error*.

For example, the estimated *standard error* of an estimated *quantity* α\^ can be computed using the bootstrap as follows:

![](https://cdn-images-1.medium.com/max/800/1*f5seqrA82RLF6RU_Y3Hk_w.png)

**References:**

\[embed\]http://www-bcf.usc.edu/\~gareth/ISL/\[/embed\]\
<https://lagunita.stanford.edu/c4x/HumanitiesScience/StatLearning/asset/cv_boot.pdf>

------------------------------------------------------------------------

*Thank you for reading my post. I regularly write about Data & Technology on* [*LinkedIn*](https://www.linkedin.com/today/posts/ankitrathi) *&* [*Medium*](https://medium.com/@rathi.ankit)*. If you would like to read my future posts then simply ‘Connect’ or ‘Follow’. Also feel free to listen to me on* [*SoundCloud*](https://soundcloud.com/ankitrathi)*.*
