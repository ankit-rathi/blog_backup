Title: Your DS Story S01E02: Artur Krochin (Confidential)
Date: 2019-02-13 16:03
Author: ankitrathi
Category: Uncategorized
Tags: Data Science, Machine Learning, Tell Your Story
Slug: your-ds-story-s01e02-artur-krochin-confidential
Status: published

![Your DS Story: Artur Krochin (Confidential)](https://cdn-images-1.medium.com/max/1200/1*8mYaeYHzqo0I29eW8qvZtQ.png)

*‘Your DS Story’ is my attempt to bridge the gap between data science professionals & data science aspirants. Here new crop of data scientists will share their experiences, struggles, achievements & their advice so that data science aspirants/enthusiasts can learn and get inspired.*

------------------------------------------------------------------------

\[embed\]https://www.linkedin.com/in/arturkrochin/\[/embed\]\
\[embed\]https://www.linkedin.com/in/arturkrochin/\[/embed\]

**1. Please tell us a bit about your background?**

My academic background is a weird mix of mathematics and computer science. Pretty much since I was 14, I was really into coding, tinkering with stuff, and developing software, but for a variety of reasons, I did mathematics at university — I figured it would be easier to learn computer science in my free time, all the while focusing on rigorous statistics and mathematics at university, and I was right; I benefited hugely from this in my career — even if I didn’t do any statistical learning in my course.

I started out as a data and machine learning engineer for a major tech consulting company. As a fresh graduate, it was hugely exciting to be part of an internal fin-tech start-up from the get-go. Our goal was to build the future of distributed transaction processing. We had an original IP — I had the chance to contribute some core features in Scala and Java, develop a unit test suite, and even add some machine learning to it. It was roughly the time when I started falling in love with data science.

An interesting problem I had to solve was at the intersection of statistics and engineering: the detection of fraudulent transactions. Looking back at it, it seems obvious, but at the time, after much prototyping, I was amazed at how an auto-encoder could be combined with network analytics to produce some great results. I have a close relationship with network analysis and visualization to this day — in fact, I’m developing a course on it for [pluralsight.com](http://pluralsight.com/).

Roughly half-way into my career at the company, I was deployed to a major British energy provider, where I was part of a software engineering team — again a start-up of sorts, as it happens — developing a one-of-a-kind data cataloging tool. Imagine you have a huge data lake and you want to make it GDPR compliant. Normally, it would take tens — if not hundreds — of meetings with all sorts of business function owners to identify what sensitive data they may be dealing with. Our tool allowed for a kind of scanning of the data lake to detect this sensitive data automatically. It took some clever engineering — took some clever machine learning algorithms to scan through columns and identify the sensitivity of data too.

Ultimately, what really excites me about data science is how you can combine theorems of some Russian statistician from the early 20th century with containers, endpoints, notebooks, gradient boosting frameworks and the like — all proud members of the 21st century techno zeitgeist. Just like that. And you get to have a huge business impact while you’re at it.

**2. What projects you are working these days?**

I now work for a major telecommunications company where my time is split somewhat evenly between engineering and data science. I’m the incumbent data scientist in customer retention, and my main concerns include preventing customer churn.

I suppose the most interesting realization about churn is that it may be manifold. Someone leaving the business — that’s churn. Someone porting out to a different operator — that’s churn. Someone downgrading to a sim-only contract — that can be churn too. From a business strategy viewpoint, each type of churner must be treated differently, e.g. there are specific campaigns targeted at people who have been identified as likely to cease their contract entirely, and then there’s a whole different set of campaigns targeted at people who merely want to switch providers. My task then becomes to build a set of intelligent propensity models capable of differentiating between different types of churn likelihood. Specifically, it is very much about hypothesizing features, building the *ETL* processes for them, and checking whether they correlate with a certain type of churn. Therein lies the “art” aspect of data science: oftentimes, it’s educated guesswork.

A major challenge for most companies is *GDPR*. We handled *GDPR* well, but naturally there were data sources we could not use anymore without proper consent. Consequently, it decreased the predictive ability of some models until substitute data sources were introduced. *GDPR* is an enormously important policy, but it’s not necessarily a data scientist’s best friend; it constrains the creative ability of a data scientist, but in the interest of ethics, as harsh as it is, it must be done.

**3. How your day to day job looks like?**

My day-to-day job is very hectic. We work in two-week sprints, which sets the rhythm for my workdays. Every day starts with a stand-up meeting where we discuss what we are doing and whether we have any blockers. Then, of course, there’s Assam tea and checking my emails. After that, there are three modes I can be in: business ideation, maintenance of legacy systems, and model building.

A big part of every data scientist’s career is to spot optimization opportunities. You’re the optimization expert after all. And often it boils down the talking to the right stakeholders. Sometimes, it’s enough to just send out an email. Sometimes, when you strongly feel there there’s vast opportunity for optimization, but the stakeholders are uncommunicative or unreceptive, you start coming up with techniques that are somewhat sneakier. It can be tough — especially in a big enterprise. It’s your responsibility as a data scientist to prove the worth of your methods and to bring about change. Even if it means first getting a PhD in human psychology.

Continuing the theme of big enterprise, one of the biggest challenges of working at one is legacy models. Sometimes, it’s a matter of maintaining models developed by people who have left. In worse cases, you have to migrate old *SAS* processes, which often involves tracing through the whole script, understanding the business logic, and replicating everything using modern tools — in my case *Python* and *XGBoost*.

The most exciting part of my profession is obviously model building. After business ideation — at which point I’ve identified an optimization opportunity and formally defined the label with a product owner — I start my initial investigation. This often involves sampling some data, testing my hypotheses, and producing some neat-looking plots. I like to use *Pandas* and *Seaborn* for this, although I’m beginning to grow fond of *Bokeh*. Obviously, all work is done in a *Jupyter* Notebook. Later, I take a set of base features most models share and see if there’s correlation between any of them and the final label — mutual information and Pearson’s correlation index work great. If there is a correlation, I tend to quickly slap together a gradient boosting model, do the usual data splits, validation and the like. Otherwise, I spend some time developing *ETL* processes for new features. It’s not surprising that some types of churn will need their own unique features that haven’t been developed yet.

When the prototype of the model is done, I present the results and evaluation metrics to the relevant stakeholders, and we collectively decide if it’s worth productionizing and tuning it. As agile dictates, we’re never too hasty to productionize or tune anything — it has to be an iterative process.

**4. How you started with DS or transitioned into DS?**

I have covered it throughout the other sections in the interview.

**5. What advice would you like to give to DS starters or DS transitioners?**

When it comes to tips for aspiring data scientists, let’s first admit one fact. There is currently a deep learning craze. A craze to the point that all data science aspirants do is learn *Tensorflow* and think they’re going to change the world with it. Truth of the matter is, if you want to become a successful data scientist, your knowledge must be more holistic. There’s a reason traditional machine learning is still used. A rule I like to use is this: if your features have names that a business-minded person could understand (average revenue per user, customer tenure, number of extra data bundles), then a traditional machine learning model should do — specifically, tree boosting, or random forest are great for most use cases. If you have weird features like aggregated pixel values or word embeddings, which is often the result of pre-processing unstructured data — that’s the perfect use case for deep learning.

Another point is statistics. A data scientist is simply a re-branded statistician who’s handy with a computer. If you don’t have a clue about Bayesian inference, A/B tests, properties of distributions, hypothesis testing and such, you’re going to have a very tough time as a data scientist.

In our day being ignorant to these areas of statistics is impermissible. There’s a plethora of *MOOCs*, videos on YouTube, and *Udacity* courses to fill in your knowledge gaps. You don’t even have to pay or get certificates — they’re useless for the most part anyway. Just watch and absorb — maybe go over some *Kaggle* notebooks, but please don’t waste all your time on *Kaggle*.

If you come from an engineering background, you really need to understand what you’re getting yourself into. You won’t be able to code away all day like before, completely unaware of the business that surrounds you. You’ll be exposed to it, you’ll live it, and you’ll have to deal with a lot of people and a lot of characters; you’ll be the underdog trying to convince business leads that using *SAS* in 2019 is maybe not that great an idea as it was 20 years ago; you’ll have to make pretty *PowerPoints* to communicate your results; you’ll have to make up three-act stories for your data exploration to get people to care, because people are people. And chances are that as an engineer, you lack the statistical background to become a data scientist immediately.

But at the same time, when your analysis is done and your *Jupyter* notebook is clocking in 12 hours; when all the plots have been plotted and stories composed, and you’re just uploading your final model propensities to the database at 8 pm on a Friday, it makes it worth it.

So, if what I said doesn’t stop you, have a go at it and good luck!

------------------------------------------------------------------------

*Thank you for reading my post. I regularly write about Data & Technology on* [*LinkedIn*](https://www.linkedin.com/today/posts/ankitrathi) *&* [*Medium*](https://medium.com/@rathi.ankit)*. If you would like to read my future posts then simply ‘Connect’ or ‘Follow’. Also feel free to listen to me on* [*SoundCloud*](https://soundcloud.com/ankitrathi)*.*
