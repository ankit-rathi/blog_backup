Title: Modern Data Architecture
Date: 2017-10-13 00:00
Author: ankitrathi
Category: Uncategorized
Tags: Big Data, Data Analytics, Data Architecture
Slug: modern-data-architecture
Status: published

![*Image Courtesy:* [*http://starworldpacknmove.com/Design-And-Architecture.html*](http://starworldpacknmove.com/Design-And-Architecture.html)](https://cdn-images-1.medium.com/max/800/0*Op5b_NUAPVC4ZHkf.jpg)

Existing data architectures are at the breaking point with the large amount of data, velocity of data ingestion, and variety of data they need to process and store. Industry analysts are predicting that up to 80% of the new data will be semi-structured and unstructured (video, pictures, audio, documents, emails, and so on) data coming from clickstream, sentiment/social media, machine sensors, server logs, RFID, and GPS (geographic).

Modern Data Architecture address the business demands for speed and agility by enabling organizations to quickly find and unify their data across hybrid data storage technologies. The Modern Data Architecture stores data as is; it does not require pre-modeling. It handles the volume, velocity, and variety of big data.

Before going deep into Modern Data Architecture, let’s start from the basics. I will cover these aspects of data architecture in this post:

*a. What is Data Architecture*

*b. History of Data Architecture*

*c. Traditional Data Architecture*

*d. Advanced Data Architecture*

*e. Modern Data Architecture*

*f. Six Principles of Modern Data Architecture*

**What is Data Architecture?**

Data Architecture is a set of rules, policies, and models that determine what kind of data gets collected, and how it gets used, processed, and stored within a database system. Data integration, for example, is dependent on Data Architecture for instructions on the integration process. Without the shift from a programming paradigm to a Data Architecture paradigm, modern computers would be much clumsier and much slower.

**History of Data Architecture**

In early days, as you can see in the diagram below, there were no distributed systems. Users were less, transactions were less so whole data architecture could be handled on single server.

![](https://cdn-images-1.medium.com/max/800/0*DUbYTmSeFQLnlBMm.png)

**Traditional Data Architecture**

Over the period of time, when more users got workstations & automated systems started generating data, Front End & Back End systems were split, which in turn increased the load on the databases. To tackle that, databases were split based on functional divisions. But this created data integrity problems for BI as different databases reported different figures and load also increased in databases from BI side. This resulted into inception of data warehouses and different data marts to cater different reporting needs.

![](https://cdn-images-1.medium.com/max/800/0*ec94HNZR2y1kjzvs.png)

**Advanced Data Architecture**

In order to solve for disaster recovery, secondary site came into picture, different replication & backup/restore options were chosen for databases & data warehouses based on their sizes but latency at the BI/Reporting side was still a problem. ELT & CDC options were considered with its own pros & cons. ELT allows raw data to be loaded directly into the target and transformed there. CDC is a set of software design patterns used to determine (and track) the data that has changed so that action can be taken using the changed data.

![](https://cdn-images-1.medium.com/max/800/0*4GykKMfi4wZ4Es5l.png)

**Modern Data Architecture**

Advanced data architecture didn’t solve for all the below mentioned problems:

1\. Time to action takes up to 7 days

2\. Amount of data is still growing

3\. DWH MPP storage is expensive

*Data Lakes & Lambda Architecture*

Above problems can be solved using Data Lakes (2nd & 3rd) & Lambda Architecture (1st). A data lake is a storage repository that holds a vast amount of raw data in its native format until it is needed. Lambda architecture is a data-processing architecture designed to handle massive quantities of data by taking advantage of both batch- and stream-processing methods.

![](https://cdn-images-1.medium.com/max/800/0*MWJ1ZUWO8KaCnzXo.png)

![](https://cdn-images-1.medium.com/max/800/0*PyYmwTyq-jaqy_Sm.png)

Still, there were few problems that needed to be addressed:

1\. Too many standby systems

2\. How to replicate Hadoop cluster?

3\. How to sync data in real-time systems?

4\. How to better sync DWH?

All of the above stated problems can be solved using Pipelining. A pipeline is a set of data processing elements connected in series, where the output of one element is the input of the next one. As you can see in the next diagram, replication queues takes some time but solve for the higher latency problems.

![](https://cdn-images-1.medium.com/max/800/0*p_X7AbQitIRzJ0z_.png)

**Six Principles of Modern Data Architecture**

1\. Data is a Shared Asset

2\. Provide the Right Interfaces for Consumption

3\. Ensure Security and Access Controls

4\. Ensure a Common Vocabulary

5\. Information Through Data Stewardship

6\. Eliminate Data Copies & Movement

**References**

1.  [*Brief History of Data Architecture*](http://www.dataversity.net/brief-history-data-architecture-shifting-paradigms/)
2.  [*Understanding the Big Data World*](http://www.pearsonitcertification.com/articles/article.aspx?p=2427073)
3.  [*Modern Data Architecture*](https://www.slideshare.net/AGrishchenko/modern-data-architecture-54850697)
4.  [*Six Principles of Modern Data Architecture*](https://vision.cloudera.com/the-six-principles-of-modern-data-architecture/)

------------------------------------------------------------------------

*Thank you for reading my post. I regularly write about Data & Technology on* [*LinkedIn*](https://www.linkedin.com/today/posts/ankitrathi) *&* [*Medium*](https://medium.com/@rathi.ankit)*. If you would like to read my future posts then simply ‘Connect’ or ‘Follow’. Also feel free to connect on or* [*Slideshare*](https://www.slideshare.net/ankitrathi)*.*

*Originally published at* <https://www.linkedin.com/today/posts/ankitrathi> *on October 13, 2017.*
