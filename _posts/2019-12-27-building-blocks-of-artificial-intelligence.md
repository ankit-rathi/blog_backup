---
toc: true
layout: post
description: Concepts to learn, Process to follow & Tools to master
categories: [markdown]
title: Building Blocks of Artificial Intelligence
---

Title: Building Blocks of Artificial Intelligence
Date: 2019-12-27 17:10
Author: ankitrathi
Category: Uncategorized
Tags: Artificial Intelligence, Building Blocks, Data Science, Machine Learning, Towards Data Science
Slug: building-blocks-of-artificial-intelligence
Status: published

![](https://cdn-images-1.medium.com/max/1200/1*jQQ7PSA9MQXa0FTdS19EHA.png)

There are a few core skills in every job. To perform that job, you need to be aware of core concepts, you need to be aware of the end to end process and you need to learn how to use related tools to perform that job. Artificial Intelligence is no different, it has its own core concepts, processes and tools.

This post covers the core concepts you need to learn, the end-to-end process you need to be aware of & important tools you need to master to work as a data scientist.

![](https://cdn-images-1.medium.com/max/800/1*rhRKmQu9vXKYuzHOftQ05Q.png)

> Please note that this post only outlines the concepts, processes and tools used by data scientists. I will publish the resources (mostly free) for these topics in upcoming post.

*Still, if you want to build a quick understanding you can refer the following post:*

\[embed\]https://medium.com/data-deft/data-science-the-complete-reference-series-3fb35077fc5a\[/embed\]

### Concepts to learn

![](https://cdn-images-1.medium.com/max/800/1*IQdUsr1L1EjjGRJTVxXzlw.png)

#### Mathematics

Artificial Intelligence contains math — no avoiding that! This section is for learners about basic math they need in order to be successful in almost any AI project/problem. So let’s start:

**Multivariate Calculus**

Calculus is a set of tools for analyzing the relationship between functions and their inputs. In Multivariate Calculus, we can take a function with multiple inputs and determine the influence of each of them separately.

In AI, we try to find the inputs which enable a function to best match the data. The slope or descent describes the rate of change off the output with respect to an input. Determining the influence of each input on the output is also one of the critical tasks. All this requires a solid understanding of Multivariate Calculus.

**Linear Algebra**

The word *algebra* comes from the Arabi word “*al-jabr*” which means “*the reunion of broken parts*”. This is the collection of methods deriving unknowns from knowns in mathematics. *Linear Algebra* is the branch that deals with *linear equations* and *linear functions* which are represented through *matrices* and *vectors*. In simpler words, it helps us understand geometric terms such as planes, in higher dimensions, and perform mathematical operations on them. By definition, algebra deals primarily with scalars (one-dimensional entities), but Linear Algebra has vectors and matrices (entities which possess two or more dimensional components) to deal with linear equations and functions.

*Linear Algebra* is central to almost all areas of mathematics like *geometry* and *functional analysis*. Its concepts are a crucial prerequisite for understanding the theory behind *AI*. You don’t need to understand *Linear Algebra* before getting started in *AI*, but at some point, you may want to gain a better understanding of how the *different algorithms* really work under the hood. So if you really want to be a professional in this field, you will have to master the parts of *Linear Algebra* that are important for *AI*.

**Statistics & Probability**

*Statistics* is a mathematical body of science that pertains to the *collection*, *analysis*, *interpretation* or *explanation*, and *presentation* of data. Probability is the chance that something will happen — how likely it is that some event will happen.

Statistics help you to understand your data and is an initial & very important step of AI. This is due to the fact that AI is all about making predictions and you can’t predict if you can’t understand the patterns in existing data.

Uncertainty and randomness occur in many aspects of our daily life and having a good knowledge of probability helps us make sense of these uncertainties. Learning about probability helps us make informed judgments on what is likely to happen, based on a pattern of data collected previously or an estimate.

AI often uses statistical inferences to predict or analyze trends from data, while statistical inferences use probability distributions of data. Hence knowing probability & statistics and its applications are important to work effectively on AI problems.

#### Programming

To execute the AI pipeline, you need to learn algorithm design as well as fundamental programming concepts such as data selection, iteration and functional decomposition, data abstraction and organisation. In addition to this, you need to learn how to perform simple data visualizations using programming and embed your learning using problem-based assignments.

#### Machine Learning Algorithms

Machine learning algorithms can be divided into 3 broad categories —

-   Supervised learning,
-   Unsupervised learning
-   Reinforcement learning.

Supervised learning is useful in cases where a property (*label*) is available for a certain dataset (*training set*) but is missing and needs to be predicted for other instances. Unsupervised learning is useful in cases where the challenge is to discover implicit relationships in a given *unlabeled* dataset (items are not pre-assigned). Reinforcement learning falls between these 2 extremes — there is some form of feedback available for each predictive step or action, but no precise label or error message.

> Intrinsic details of various algorithms is not in scope of this series, you can refer the resources mentioned in the next post to learn them.

Supervised learning can be further divided into Regression (Linear, Non-linear, etc) & Classification (Logistics Regression, Decision Tree, Naïve Bayes etc) algorithms. Some algorithms can be used for regression as well as classification i.e. Random Forests, Support Vector Machines, etc.

Unsupervised learning can also be further divided into Clustering, Anomaly Detection, Associative Mining.

Reinforcement learning is an area of machine learning concerned with how software agents ought to take actions in an environment so as to maximize some notion of cumulative reward.

#### Deep Learning Frameworks

Deep learning frameworks are a more advanced form of ML and solve specific problems where data is either unstructured or huge or both. Neural Nets, CNNs, RNNs & LSTM, GANs are the frameworks one needs to be aware of.

\[embed\]https://medium.com/data-deft/data-science-the-complete-reference-series-3fb35077fc5a\[/embed\]

#### Domain Knowledge

This lack of domain knowledge, while perfectly understandable, can be a major barrier to data scientists. For one thing, it’s difficult to come up with project ideas in a domain that you don’t know much about. It can also be difficult to determine the type of data that may be helpful for a project — if you want to build a model to predict an outcome, you need to know what types of variables might be related to this outcome so you can make sure to gather the right data.

Knowing the domain is useful not only for figuring out projects and how to approach them but also for having rules of thumb for sanity checks on the data. Knowing how data is captured (is it hand-entered? Is it from machines that can give false readings for any number of reasons?) can help a data scientist with data cleaning and from going too far down the wrong path. It can also inform what true outliers are and which values might just be due to measurement error.

Often the most challenging part of building a machine learning model is feature engineering. Understanding variables and how they relate to an outcome is extremely important for this. Knowing the domain can help direct the data exploration and greatly speed (and enhance) the feature engineering process.

Once features are generated, knowing what relationships between variables are plausible help for basic sanity checks. Being able to glance at the outcome of a model and determine if they make sense goes a long way for quality assurance of any analytical work.

> Finally, one of the biggest reasons a strong understanding of the data is important is because you have to interpret the results of analyses and modeling work.

Knowing what results are important and which are trivial is important for the presentation and communication of results. It’s also important to know what results are actionable.

### Process to follow

![](https://cdn-images-1.medium.com/max/800/1*TPtwP0mAlx6JGjSiJCy18g.png)

#### Problem Definition

The first thing you have to do before you solve a problem is to define exactly what it is. You need to be able to translate data questions into something actionable.

You’ll often get ambiguous inputs from the people who have problems. You’ll have to develop the intuition to turn scarce inputs into actionable outputs–and to ask the questions that nobody else is asking.

#### Data Collection

Once you’ve defined the problem, you’ll need data to give you the insights needed to turn the problem around with a solution. This part of the process involves thinking through what data you’ll need and finding ways to get that data, whether it’s querying internal databases, or purchasing external data-sets.

#### Data Understanding

The difficulty here isn’t coming up with ideas to test, it’s coming up with ideas that are likely to turn into insights. You’ll have a fixed deadline for your AI project, so you’ll have to prioritize your questions.

You’ll have to look at some of the most interesting patterns that can help explain why sales are reduced for this group. You might notice that they don’t tend to be very active on social media, with few of them having Twitter or Facebook accounts. You might also notice that most of them are older than your general audience. From that you can begin to trace patterns you can analyze more deeply.

#### Feature Engineering

Feature engineering is the process of using domain knowledge of the data to create features that make machine learning algorithms work. If feature engineering is done correctly, it increases the predictive power of machine learning algorithms by creating features from raw data that help facilitate the machine learning process. Feature Engineering is, in fact, an art.

#### Modelling

Depending on the type of question that you’re trying to answer, there are many modelling algorithms available. You run the selected algorithm/s on the training data to build the models.

#### Validation

Validation is a step used to evaluate the trained model on validation data. You use a series of competing for machine-learning algorithms along with the various associated tuning parameters that are geared toward answering the question of interest with the current data.

#### Tuning

Tuning an algorithm or machine learning technique can be simply thought of as a process which one goes through in which they optimize the parameters that impact the model in order to enable the algorithm to perform the best.

#### Deployment

After you have a set of models that perform well, you can operationalize them for other applications to consume. Depending on the business requirements, predictions are made either in real-time or on a batch basis. To deploy models, you expose them with an open API interface. The interface enables the model to be easily consumed from various applications.

### Tools to master

![](https://cdn-images-1.medium.com/max/800/1*Y0AVQ5pq0t0NKEec9AXxZQ.png)

> The list mentioned here is not exhaustive, it depends more on what kind of problem you are solving and in what tech stack you are working.

#### SQL

Structured Query Language (SQL) is a standard computer language for relational database management and data manipulation. SQL is used to query, insert, update and modify data. Most relational databases support SQL.

As data collection has increased exponentially, so has the need for people skilled at using and interacting with data; to be able to think critically, and provide insights to make better decisions and optimize their businesses. The skills necessary to be a good data scientist include being able to retrieve and work with data and to do that you need to be well versed in SQL, the standard language for communicating with database systems.

\[embed\]https://medium.com/data-deft/data-science-the-complete-reference-series-3fb35077fc5a\[/embed\]

#### R

R is a programming language and software environment for statistical analysis, graphics representation and reporting. In the world of AI, R is an increasingly popular language for a reason. It was built with statistical manipulation in mind, and there’s an incredible ecosystem of packages for R that let you do amazing things — particularly in data visualization.

\[embed\]https://medium.com/data-deft/data-science-the-complete-reference-series-3fb35077fc5a\[/embed\]

#### Python

Python is a general-purpose interpreted, interactive, object-oriented, and high-level programming language. Python is no-doubt the best-suited language for a Data Scientist. It is a free, flexible and powerful open-source language. Python cuts development time in half with its simple and easy to read syntax. With Python, you can perform data manipulation, analysis, and visualization. Python provides powerful libraries for Machine learning applications and other scientific computations.

\[embed\]https://medium.com/data-deft/data-science-the-complete-reference-series-3fb35077fc5a\[/embed\]

#### Tensorflow

Currently, the most famous deep learning library in the world is Google’s TensorFlow. Google product uses machine learning in all of its products to improve the search engine, translation, image captioning or recommendations.

TensorFlow is the best library of all because it is built to be accessible to everyone. Tensorflow library incorporates different API to built at scale deep learning architecture like CNN or RNN. TensorFlow is based on graph computation; it allows the developer to visualize the construction of the neural network with Tensorboad. This tool is helpful to debug the program. Finally, Tensorflow is built to be deployed at scale. It runs on CPU and GPU.

\[embed\]https://medium.com/data-deft/data-science-the-complete-reference-series-3fb35077fc5a\[/embed\]

#### Keras

Keras is a high-level neural networks API, capable of running on top of Tensorflow, Theano, and CNTK. It enables fast experimentation through a high level, user-friendly, modular and extensible API.

Keras allows for easy and fast prototyping (through user-friendliness, modularity, and extensibility). It supports both convolutional networks and recurrent networks, as well as combinations of the two. It runs seamlessly on CPU and GPU.

\[embed\]https://medium.com/data-deft/data-science-the-complete-reference-series-3fb35077fc5a\[/embed\]

So this is all that I needed to cover in this article. Now you know what concepts you need to learn, the process you need to follow and the tools you need to master in order to get proficient in the field of AI.

------------------------------------------------------------------------

[*Ankit Rathi*](https://www.ankitrathi.com/) *is an AI architect, published author & well-known speaker. His interest lies primarily in building end-to-end AI applications/products following best practices of Data Engineering and Architecture.*

*Why don’t you connect with Ankit on* [*Twitter*](https://twitter.com/rathiankit)*,* [*LinkedIn*](https://www.linkedin.com/in/ankitrathi/) *or* [*Instagram*](https://instagram.com/ankitrathi/)*?*
