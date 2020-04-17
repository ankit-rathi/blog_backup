Title: Multivariate Calculus for Data Science
Date: 2019-01-05 12:56
Author: ankitrathi
Category: Uncategorized
Tags: Data Science, Machine Learning
Slug: multivariate-calculus-for-data-science
Status: published

![](https://cdn-images-1.medium.com/max/1200/1*aq2ZmNZnloBbd1sxGNdSzw.png)

*This is the 4th post of blog post series ‘*[*Data Science: The Complete Reference*](https://medium.com/@rathi.ankit/data-science-the-complete-reference-series-3fb35077fc5a)*’, this post covers these topics related to data science introduction.*

-   *What is Multivariate Calculus?*
-   *Why Multivariate Calculus is important in Data Science?*
-   *How Multivariate Calculus is applied in Data Science?*

------------------------------------------------------------------------

> Visit [ankitrathi.com](http://ankitrathi.com/) now to:

> — to read my blog posts on various topics of AI/ML

> — to keep a tab on latest & relevant news/articles daily from AI/ML world

> — to refer free & useful AI/ML resources

> — to buy my books on discounted price

> — to know more about me and what I am up to these days

### *What is Multivariate Calculus?*

*Multivariate Calculus (also known as multivariable calculus) is the extension of calculus in one variable to calculus with functions of several variables: the differentiation and integration of functions involving multiple variables, rather than just one. \~Wikipedia*

Calculus is a set of tools for analyzing the relationship between functions and their inputs. In Multivariate Calculus we can take a function with multiple inputs and determine the influence of each of them separately.

![<https://www.toppr.com/bytes/multivariable-calculus/>](https://cdn-images-1.medium.com/max/800/0*biYt3XYDs6oPHtj8.png)

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

### *Why Multivariate Calculus is important in Data Science?*

In data science, we try to find the inputs which enable a function to best match the data. The slope or descent describes the rate of change off the output with respect to an input. Determining the influence of each input on the output is also one of the critical tasks. All this requires solid understanding of Multivariate Calculus.

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

### *How Multivariate Calculus is applied in Data Science?*

First, lets cover core concepts of Calculus:

#### Functions

An equation will be a function if, for any x in the domain of the equation, the equation will yield exactly one value of y when we evaluate the equation at a specific x.

y = f(x)

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

#### Derivatives

The derivative of f(x) with respect to *x* is the function f′(x) and is defined as:

![](https://cdn-images-1.medium.com/max/800/1*UFil9GeVK6rdFWBIjtWf1g.png)

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

#### Product Rule

If the two functions f(x) and g(x) are differentiable (*i.e.* the derivative exist) then the product is differentiable and:

![](https://cdn-images-1.medium.com/max/800/1*NVd5IXnpcP_yY06lbTDanQ.png)

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

#### Chain Rule

Suppose that we have two functions f(x) and g(x) and they are both differentiable.

-   If we define F(x)=(f∘g)(x) then the derivative of F(x) is:

![](https://cdn-images-1.medium.com/max/800/1*P8lcz4wNwol-_xRw_81xgg.png)

-   If we have y=f(u) and u=g(x) then the derivative of y is:

![](https://cdn-images-1.medium.com/max/800/1*vMT2wHGpnZSSEjAZHprCOQ.png)

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

#### Integrals

If *F(x)* is any anti-derivative of *f(x)* then the most general anti-derivative of *f(x)* is called an *indefinite integral* and denoted:

![](https://cdn-images-1.medium.com/max/800/1*eDOFI30E-ZMQalR-Et84VQ.png)

c is any constant

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

Given a function *f(x)* that is continuous on the *interval \[a,b\]* we divide the interval into n subintervals of equal width (*Δx)* and from each interval choose a point, *x∗i*. Then the *definite integral of f(x) from a to b* is:

![](https://cdn-images-1.medium.com/max/800/1*OnGVkNlzH68c-kX3AsOuKw.png)

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

#### Partial Derivatives

A partial derivative of a function of several variables is its derivative with respect to one of those variables, with the others held constant (as opposed to the total derivative, in which all variables are allowed to vary).

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

Now, lets look at the core concepts of Multivariate Calculus & how those relate to Data Science:

#### The Gradient

Gradients show changes along a particular variable or set of variables as a function “move” in space, and they are very easy to compute within optimization frameworks. The algorithms find minima/maxima of these functions and base optimization on these estimates.

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

#### The Jacobian

The Jacobian of a set of functions is a matrix of partial derivatives of the functions. If you have just one function instead of a set of function, the Jacobian is the gradient of the function.

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

#### The Hessian

Hessian is, in some crude sense, rate of change of rate of change of the function. In regards to optimization, Hessian being positive definite, negative definite or indefinite tells you about whether the optima in question is a maxima, minima or a saddle point.

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

#### Multivariate Chain Rule

Suppose that *z*=*f*(*x,y*), where *x* and *y* themselves depend on one or more variables. Multivariable Chain Rules allow us to differentiate *z* with respect to any of the variables involved:

![](https://cdn-images-1.medium.com/max/800/1*SkQnNxcOM6JXu52VhNDofQ.png)

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

#### Approximate Functions

A *function approximation* problem asks us to select a function among a well-defined class that closely matches (“approximates”) a target function.

Statistical and connectionist approaches to machine learning are related to function approximation methods in mathematics.

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

Common techniques include the *Taylor series and the Fourier series* approximations. Recall that given enough terms, a Taylor series can approximate *any function* to a certain level of precision about a given point, while a Fourier series can approximate *any periodic function*.

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

#### Power Series

A power series is any series that can be written in the form where a and cn are numbers. The cn’s are often called the coefficients of the series. The first thing to notice about a power series is that it is a function of x.

![](https://cdn-images-1.medium.com/max/800/1*gXToTGg5ESS1xCXKV058kQ.png)

In data science, *Power Series* can be used to give you some indication of the size of the error, that results from using these approximations.

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

#### Linearisation

Linearisation is finding the linear approximation to a function at a given point. The linear approximation of a function is the first order Taylor expansion around the point of interest.

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

#### Multivariate Taylor

A Multivariate Taylor series is an idea used in data science and other kinds of higher-level mathematics. It is a series that is used to create an estimate (guess) of what a function looks like with multiple inputs.

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

Multivariate Taylor is the Power Series to its more general multivariate form.

### References

\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]\
\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]\
\[embed\]https://www.khanacademy.org/math/multivariable-calculus\[/embed\]

------------------------------------------------------------------------

*Thank you for reading my post. I regularly write about Data & Technology on* [*LinkedIn*](https://www.linkedin.com/today/posts/ankitrathi) *&* [*Medium*](https://medium.com/@rathi.ankit)*. If you would like to read my future posts then simply ‘Connect’ or ‘Follow’. Also feel free to listen to me on* [*SoundCloud*](https://soundcloud.com/ankitrathi)*.*
