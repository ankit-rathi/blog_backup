---
toc: true
layout: post
description: Commonly Used Framework For DS/AI Projects
categories: [markdown]
title: Data Science Framework
---

![](https://cdn-images-1.medium.com/max/800/0*OOZpGGVL8g-7_GAh.jpg)

A lot of material is available on ‘how to learn machine learning (ML)/data science (DS)?’ but when we work on actual ML/DS project, we realize that the core aspects (modeling & evaluation) that we learnt is actually just a small part of the overall solution. When working as a data scientist, nobody tells us whats the ML/DS problem that we need to solve or the prediction that we need to make, we need to understand the business process first and identify the problem and qualify the problem suitable for a ML/DS solution.

Then we need to collect underlying data being used by the business and assess whether its enough & useful to convert this business problem to ML/DS problem. Further, we explore the data & prepare it to be consumed by prediction algorithms/models & evaluate the model performance before deploying the model in production. In between, we also need to identify a suitable evaluation methodology & agree monitoring & support activities with business.

In this article, I will cover these aspects to give you a holistic view of Data Science Framework built on CRISP/DM methodology:

-   Business understanding
-   Data understanding
-   Data preparation
-   Modeling
-   Evaluation
-   Deployment

*These three activities are performed in iterative manner to reach most optimized & generalized model avoiding under-fitting or over-fitting.*

*Data preparation \<-\> Modeling \<-\> Evaluation*

**Business understanding**

This initial phase focuses on understanding the project objectives and requirements from a business perspective, then converting this knowledge into a data science problem definition and a preliminary plan designed to achieve the objectives.

-Define the business problem

-Set the criteria for success

-Convert business problem to DS problem

-Categorize the DS problem (Classification/Regression/Anomaly Detection etc)

-Prepare a high-level plan to achieve results

-Visulaize the DS pipeline in context of objective (Evaluation Criteria/Algorithms/Transformations)

**Data understanding**

The data understanding phase starts with initial data collection and proceeds with activities that enable you to become familiar with the data, identify data quality problems, discover first insights into the data, and/or detect interesting subsets to form hypotheses regarding hidden information.

-Collect & integrate initial data

-Understand the attributes & its relationship

-Identify data quality issues

-Perform EDA (Exploratory Data Analysis)

**Data preparation**

The data preparation phase covers all activities needed to construct the final dataset from the initial raw data. Data preparation tasks are likely to be performed multiple times and not in any prescribed order. Tasks include table, record, and attribute selection, as well as transformation and cleaning of data for modeling tools.

-Integrate data sources

-Handle missing values, outliers

-Apply Feature Engineering

**Modeling**

In this phase, various modeling techniques are selected and applied, and their parameters are calibrated to optimal values. Typically, there are several techniques for the same data mining problem type. Some techniques have specific requirements on the form of data. Therefore, going back to the data preparation phase is often necessary.

-Apply multiple models

-Choose most optimal model

-Create a feedback pipeline

-Ensemble/Stack different models

**Evaluation**

Before proceeding to final deployment of the model, it is important to thoroughly evaluate it and review the steps executed to create it, to be certain the model properly achieves the business objectives. A key objective is to determine if there is some important business issue that has not been sufficiently considered. At the end of this phase, a decision on the use of the data science results should be reached.

-Refine evaluation criteria

-Evaluate the models

-Handle Overfitting/Underfitting

**Deployment**

Depending on the requirements, the deployment phase can be as simple as generating a report or as complex as implementing a repeatable DS process across the enterprise. In many cases, it is the customer, not the data analyst, who carries out the deployment steps. However, even if the analyst will carry out the deployment effort, it is important for the customer to understand up front what actions need to be carried out in order to actually make use of the created models.

-Prepare a detailed deployment plan

-Agree on post-deployment monitoring & support

-Monitor & support

**Reference**

[CRISP-DM Guide](https://www.the-modeling-agency.com/crisp-dm.pdf)

[Data science framework overview](http://datascienceguide.github.io/data-science-framework)

[EDISON Data Science Framework to define the Data Science Profession](http://www.kdnuggets.com/2016/10/edison-data-science-framework.html)

------------------------------------------------------------------------

*Thank you for reading my post. I regularly write about Data & Technology on* [*LinkedIn*](https://www.linkedin.com/today/posts/ankitrathi) *&* [*Medium*](https://medium.com/@rathi.ankit)*. If you would like to read my future posts then simply ‘Connect’ or ‘Follow’. Also feel free to connect on* [*Slideshare*](https://www.slideshare.net/ankitrathi)*.*

*Originally published at* <https://www.linkedin.com/today/posts/ankitrathi> *on August 14, 2017.*
