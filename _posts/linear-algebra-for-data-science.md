Title: Linear Algebra for Data Science
Date: 2018-12-28 13:12
Author: ankitrathi
Category: Uncategorized
Tags: Data Science, Machine Learning
Slug: linear-algebra-for-data-science
Status: published

![](https://cdn-images-1.medium.com/max/1200/1*BrXSOz_5WlU5HGqa5Q44Sw.png)

*This is the 3rd post of blog post series ‘*[*Data Science: The Complete Reference*](https://medium.com/@rathi.ankit/data-science-the-complete-reference-series-3fb35077fc5a)*’, this post covers these topics related to data science introduction.*

-   *What is Linear Algebra?*
-   *Why Linear Algebra is important in Data Science?*
-   *How Linear Algebra is applied in Data Science?*

------------------------------------------------------------------------

> Visit [ankitrathi.com](http://ankitrathi.com/) now to:

> — to read my blog posts on various topics of AI/ML

> — to keep a tab on latest & relevant news/articles daily from AI/ML world

> — to refer free & useful AI/ML resources

> — to buy my books on discounted price

> — to know more about me and what I am up to these days

### What is Linear Algebra?

*Linear algebra is the branch of mathematics concerning linear equations, linear functions and their representations through matrices and vector spaces. \~Wikipedia*

![<https://ocw.mit.edu/courses/mathematics/18-700-linear-algebra-fall-2013/>](https://cdn-images-1.medium.com/max/800/0*7ihy18VxFPzSrcIe.jpg)

The word *algebra* comes from the Arabi word “*al-jabr*” which means “*the reunion of broken parts*”. This is collection of methods deriving unknowns from knowns in mathematics. *Linear Algebra* is the branch that deals with *linear equations* and *linear functions* which are represented through *matrices* and *vectors*. In simpler words, it helps us understand geometric terms such as planes, in higher dimensions, and perform mathematical operations on them. By definition, algebra deals primarily with scalars (one-dimensional entities), but Linear Algebra has vectors and matrices (entities which possess two or more dimensional components) to deal with linear equations and functions.

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]\
\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]\
\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

### Why Linear Algebra is significant in Data Science?

*Linear Algebra* is central to almost all areas of mathematics like *geometry* and *functional analysis*. Its concepts are a crucial prerequisite for understanding the theory behind *Data Science*. You don’t need to understand *Linear Algebra* before getting started in *Data Science*, but at some point, you may want to gain a better understanding of how the *different algorithms* really work under the hood. So if you really want to be a professional in this field, you will have to master the parts of *Linear Algebra* that are important for *Data Science*.

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

### How Linear Algebra is used in Data Science?

#### Scalars, Vectors, Matrices and Tensors

-   A *scalar* is a single number
-   A *vector* is an array of numbers.
-   A *matrix* is a 2-D array
-   A *tensor* is a n-dimensional array with n\>2

![](https://cdn-images-1.medium.com/max/800/0*TV1cNycZKXbCAndD.png)

With *transposition* we can convert a *row vector* to a *column vector* and vice versa.

![Matrix Transposition](https://cdn-images-1.medium.com/max/800/0*4CaV9I1qOAgVHCvH.png)

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

#### Multiplying Matrices and Vectors

The dot product of matrices & vectors is used in every equation explaining data science algorithms. Matrices multiplication is *distributive*, *associative*, *NOT commutative*, while vector multiplication is *commutative*.

![Matrix Multiplication](https://cdn-images-1.medium.com/max/800/0*NGVp25AqACKt-YLL.png)

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

#### Identity and Inverse Matrices

The *identity matrix* *In* is a special matrix of shape (n×n) that is filled with 0 except the diagonal that is filled with 1. An *inverse matrix* is that results in the identity matrix when it is multiplied by its original form.

![Identity Matrix](https://cdn-images-1.medium.com/max/800/0*Qa4EcIg2t8cHpuxf.png)

![Inverse Matrix](https://cdn-images-1.medium.com/max/800/1*QOfLoaWKItaX5aiaY_OFLg.png)

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

#### Linear Dependence and Span

We cover here how to represent systems of equations graphically, how to interpret the number of solutions of a system, what is linear combination, dependence and span.

![](https://cdn-images-1.medium.com/max/800/0*UxuX5smKnnlkIr02.png)

![<http://algebra.math.ust.hk/vector_space/06_span/lecture2.shtml>](https://cdn-images-1.medium.com/max/800/0*itRKlIExzhIiSKF4.gif)

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

#### Norms

The *norm* is what is generally used to *evaluate* the *error of a model*. For instance it is used to calculate the *error* between the *output* of a neural network and what is *expected* (the actual label or value).

![*The squared L2 norm*](https://cdn-images-1.medium.com/max/800/0*ycES0MPNHwey0kC9.png)

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

#### Special Kinds of Matrices and Vectors

This section covers different interesting type of matrices with specific properties i.e. *Diagonal*, *Symmetric* & *Orthogonal* matrices.

![](https://cdn-images-1.medium.com/max/800/0*oP0tJyMlHRbD0SFQ.png)

![](https://cdn-images-1.medium.com/max/800/0*ivbVWUYn-71vEpfS.png)

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

#### Eigendecomposition

The *eigendecomposition* is one form of matrix *decomposition*. Decomposing a matrix means that we want to find a product of matrices that is equal to the initial matrix. In the case of the eigendecomposition, we decompose the initial matrix into the product of its *eigenvectors* and *eigenvalues*.

The eigendecomposition of the matrix corresponding to a *quadratic equation* can be used to find the *minimum* and *maximum* of that function.

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

#### Singular Value Decomposition (SVD)

The way to go to decompose other types of matrices that can’t be decomposed with *eigendecomposition* is to use *SVD*. With the SVD, we *decompose* a matrix in three other matrices. We can see these new matrices as *sub-transformations* of the space. Instead of doing the transformation in one movement, we decompose it in *three movements*.

![](https://cdn-images-1.medium.com/max/800/0*Qx3gjpWd5qF4CSs-.png)

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

#### The Moore Penrose Pseudoinverse

The *inverse* is used to solve system of equations but not all matrices have an *inverse*. In some cases, a system of equation has no solution, and thus the inverse doesn’t exist. However it can be useful to find a value that is almost a solution (in term of *minimizing* the *error*). We can find the best-fit line of a set of data points with the *pseudoinverse*.

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

#### The Trace Operator

The trace is the sum of all values in the diagonal of a *square matrix*. It can be used to specify the *Frobenius norm* of a matrix, which is needed for the *Principal Component Analysis* (PCA)

![](https://cdn-images-1.medium.com/max/800/0*9qdJapqojKTilWh3.png)

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

#### The Determinant

The determinant of a matrix AA is a number corresponding to the *multiplicative change* you get when you transform your space with this matrix. A negative determinant means that there is a change in orientation (and not just a rescaling and/or a rotation).

![](https://cdn-images-1.medium.com/max/800/0*zC1WQTrT0tfeCaxw.png)

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

#### Principal Component Analysis

When the data-set is high-dimensional, it would be nice to have a way to reduce these dimensions while keeping all the information present in the data-set. The aim of principal components analysis (PCA) is generally to reduce the number of dimensions of a data-set where dimensions are not completely decorrelated.

![](https://cdn-images-1.medium.com/max/800/0*Xi21_1lNMgM6Cxcg.png)

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

### References

\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]\
\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]\
\[embed\]https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/\[/embed\]

------------------------------------------------------------------------

*Thank you for reading my post. I regularly write about Data & Technology on* [*LinkedIn*](https://www.linkedin.com/today/posts/ankitrathi) *&* [*Medium*](https://medium.com/@rathi.ankit)*. If you would like to read my future posts then simply ‘Connect’ or ‘Follow’. Also feel free to listen to me on* [*SoundCloud*](https://soundcloud.com/ankitrathi)*.*
