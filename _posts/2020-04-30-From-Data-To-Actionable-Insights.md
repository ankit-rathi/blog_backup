---
toc: true
layout: post
description: A series of blog-posts on Data & AI Platform Concepts
categories: [markdown]
title: From Data To Actionable Insights
---

![](https://miro.medium.com/max/2000/1*vJu3xpSgK6X0T_jfUnh5_A.png)

---

> ## Data is the new oil, AI is the new electricity.

You may keep hearing these terms of late. As Data & AI field is gaining immense traction, every organization or business is looking to make the most of the opportunities available to them.

Many of you may be working on relevant projects as well, where you collect, store, process, analyse data, and serve the insights to business stakeholders. Some of you may be using the latest ML/AI techniques in your projects and may be aware of CRISP-DM technique.

If you are working on a one-off project in the AI/ML area, it is fine to just get the work done but if you have many use-cases, it makes sense to have a streamlined approach, for data ingestion, storage, processing and service, so that common resources (data, pipelines, infra etc) can be used across use cases. That’s where design, architecture & governance come into the picture.

In this article, I would like to show you the typical design of data-intensive applications using a data platform.

> *Data & AI being a vast field having many sub-fields, a single post is not enough to explain each component to sufficient depth, so I will cover the in-depth view of each component/function in upcoming posts.*

## Data & Actionable Insights
![](https://miro.medium.com/max/1400/1*T1WfVLbR0uwfNzBEhQBmtw.png)
On the highest level of abstraction, you can see a data & AI system as a black box, where data goes in and actionable insights come out. Let's look at what’s there in this black-box.

## Core & Support Functions
![](https://miro.medium.com/max/1400/1*AX1iXOcu0SFMKPVd21rvLA.png)
If you look into this black-box, you can see that there are some core functions and some support functions to transform data into actionable insights. Core functions work on data while support functions manage and optimize core functions.

## Understanding the Big Picture
![](https://miro.medium.com/max/1400/1*yqeLNbPxe1BlrQk-z0__Iw.png)
In a typical data analytics platform, there are four core functions and three support functions. Core functions provide functional requirements while support functions facilitate the non-functional requirements.

As part of core functions, data is ingested, stored, processed, analysed and served to business stakeholders to fulfil Data & AI use cases.

Support functions take care of infrastructure, security, performance, scalability and delivery aspects of these use cases.

Let’s have a look at each one of them:

## Data Ingestion
![](https://miro.medium.com/max/1400/1*CrN_yrcBei0le6t_4mHf2g.png)
Data Ingestion deals with all the challenges related to incoming data. Its a framework that makes it easier to collect and integrate data from different types of data sources and support different types of data transport protocols.

Some of the challenges faced here are: multiple source ingestion, managing streaming/real-time data, speed of ingestion, change detection.

## Data Storage
![](https://miro.medium.com/max/1400/1*DQF7xxPaLroHsoCCahxHWw.png)
Once you have ingested data into your platform, you need to store it somewhere. There are different types of storages/databases and we select specific storages/databases keeping various factors in mind like data type, ingestion type, processing and request types.

Notable storage types used in typical data platforms are file storage, Databases, Data Warehouses, Data Lakes, Delta Lakes, Data Mesh etc.

## Data Processing & Analysis
![](https://miro.medium.com/max/1400/1*qVM7MkscynGujkc0Z0opGQ.png)
To draw insights from data, we may need to clean, impute, analyse, transform, aggregate it. We may need to build meaningful features in order to build useful models. All these activities are taken care of in this function.

Data engineering, Big Data processing, Business Intelligence, Machine Learning and Artificial Intelligence capabilities are applied to the data as part of this function.

Apart from raw data, we may need to store intermediate data or derived insights in order to consume it later. Hence processing, analysis and storage functions may be used iteratively.

## Data Service
![](https://miro.medium.com/max/1400/1*qVM7MkscynGujkc0Z0opGQ.png)
Actionable insights have to be consumed by business stakeholders and customers. Data service function takes care of hosting these insights. The type of data service can be APIs, KPI reports/dashboards, notebooks and development environments.

## Cloud Services
![](https://miro.medium.com/max/1400/1*2fGS-Ja0FBLpZkOMS9RbOA.png)
All the above functions (as well as DevOps & Governance functions) can be built on-premise as well as on-cloud. Due to various benefits in terms of infrastructure, platform & application, the cloud has become go to support function for almost all the technology requirements.

Type of cloud services is available as follows: IaaS, PaaS & SaaS. Major cloud providers in Data & AI area are AWS, Azure & GCP. We will learn more about these terms in upcoming posts.

## DevOps
![](https://miro.medium.com/max/1400/1*2fGS-Ja0FBLpZkOMS9RbOA.png)
The term DevOps is a combination of two words namely Development and Operations. DevOps is a function that allows a single team to manage the entire application development life cycle, that is, development, testing, deployment, and monitoring.

The ultimate goal of DevOps is to decrease the duration of the system’s development life cycle while delivering features, fixes, and updates frequently in close synchronization with business objectives.

It consists of various stages such as continuous development, continuous integration, continuous testing, continuous deployment, and continuous monitoring.

Notable tools in DevOps area are Git, Jenkins, Kubernetes, Chef, Nagios etc.

## Governance
![](https://miro.medium.com/max/1400/1*2fGS-Ja0FBLpZkOMS9RbOA.png)
Data governance is a function to manage the availability, usability, integrity and security of the data in enterprise systems, based on internal data standards and policies that also control data usage. Effective data governance ensures that data is consistent and trustworthy and doesn’t get misused.

This function also includes other concepts such as Data Stewardship, Data Quality, and others to help an enterprise gain better control over its data assets, including methods, technologies, and behaviours around the proper management of data.

## Putting It All Together
![](https://miro.medium.com/max/1400/1*vR8dBkIDd_E6OvISB4vFNw.png)

So this post, though it was a high-level view, we learnt about how actionable insights are generated from data. I believe you found this post helpful, we will dive deeper into the above components/functions in upcoming posts.

---
[*Ankit Rathi*](https://www.ankitrathi.com/) *is an AI architect, published author & well-known speaker. His interest lies primarily in building end-to-end AI applications/products following best practices of Data Engineering and Architecture.*

*Why don’t you connect with Ankit on* [*YouTube*](https://www.youtube.com/channel/UCrIv4EU2tFX8VhhT0oCnDnw)*,* [*Twitter*](https://twitter.com/rathiankit)*,* [*LinkedIn*](https://www.linkedin.com/in/ankitrathi/) *or* [*Instagram*](https://instagram.com/ankitrathi/)*?*
