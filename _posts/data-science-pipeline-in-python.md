Title: Data Science Pipeline in Python
Date: 2018-07-28 11:07
Author: ankitrathi
Category: Uncategorized
Tags: Data Pipeline, Data Science, Github, Python3
Slug: data-science-pipeline-in-python
Status: published

![Data Science Pipeline in Python](https://cdn-images-1.medium.com/max/1200/1*lzaT8rmXUdHMi9Sx1zjwYw.jpeg)

> Visit [ankitrathi.com](http://ankitrathi.com/) now to:

> — to read my blog posts on various topics of AI/ML

> — to keep a tab on latest & relevant news/articles daily from AI/ML world

> — to refer free & useful AI/ML resources

> — to buy my books on discounted price

> — to know more about me and what I am up to these days

We all look for code-snippets while working on data science/machine learning problems, be it a case study, a competition or a project. Many data scientists have their own repositories of code-snippets to save time and focus on the problem itself rather than juggling between codes over internet.

Today, I am going to share with you my own python code repository which I have arranged and generalized into a kind of data science pipeline, from importing libraries to tuning the hyper-parameters, everything is there, you just need to customize it a bit based on your own data-set or problem.

Please note that its a basic pipeline, you still might need to write some code to implement something specific to your problem. While I have pasted the code-snippets in this blog itself, you can refer my python notebook on GitHub to get properly formatted code.

Happy coding….

\[embed\]https://github.com/ankitrathi169/Data-Science-with-Python/blob/master/DataSciencePipeline.ipynb\[/embed\]

-   **Import libraries**

> \# import basic libraries\
> import numpy as np \
> import pandas as pd \
> import warnings\
> warnings.filterwarnings(‘ignore’)

> \# import plot libraries\
> import seaborn as sns\
> sns.set\_palette(‘Set2’)\
> import matplotlib.pyplot as plt\
> %matplotlib inline

> \# import ml libraries\
> from sklearn.metrics import confusion\_matrix\
> from sklearn.preprocessing import LabelEncoder, MinMaxScaler\
> from sklearn.model\_selection import train\_test\_split, cross\_val\_score\
> from sklearn import linear\_model, datasets\
> from sklearn.ensemble import RandomForestClassifier, RandomForestRegressor\
> from sklearn.metrics import accuracy\_score\
> from sklearn.svm import LinearSVC, SVC

> \# list number of files\
> import os\
> print(os.listdir(“data”))

-   **Read data**

> \# read data

> from subprocess import check\_output\
> print(check\_output(\[“ls”, “../input/”\]).decode(“utf8”))

> train = pd.read\_csv(“data/train.csv”)\
> test = pd.read\_csv(“data/test.csv”)

-   **Check shape**

> \# check shape

> print(“Train rows and columns : “, train.shape)\
> print(“Test rows and columns : “, test.shape)

-   **Check column types**

> \# check column types

> ctype = train.dtypes.reset\_index()\
> ctype.columns = \[“Count”, “Column Type”\]\
> ctype.groupby(“Column Type”).aggregate(‘count’).reset\_index()

> train.info()

-   **Display data header**

> \# display data header

> train.head()

-   **Numerical data distribution**

> \# numerical data distribution

> train.describe()

-   **Categorical data distribution**

> \# categorical data distribution

> train.describe(include=\[‘O’\])

-   **Check missing values**

> \# check missing values\
> missing\_df = train.isnull().sum(axis=0).reset\_index()\
> missing\_df.columns = \[‘column\_name’, ‘missing\_count’\]\
> missing\_df = missing\_df\[missing\_df\[‘missing\_count’\]\>0\]\
> missing\_df = missing\_df.sort\_values(by=’missing\_count’)\
> missing\_df

-   **Impute/treat missing values**

> \# impute/treat missing values

> train\[‘col1’\] = train\[‘col1’\].fillna(train\[‘col1’\].value\_counts().index\[0\]) \# for categorical

> train\[‘col2’\].fillna(train\[‘col2’\].mean(), inplace=True) \# for numerical (mean or median)

-   **Check outliers**

> \# check ouliers

> train.ix\[np.abs(train.col-fmean) \> (3\*fstd), ‘col’\] \# upper outliers\
> train.ix\[np.abs(train.col-fmean) \< -(3\*fstd), ‘col’\] \# lower outliers

-   **Treat outliers**

> \# treat outliers

> fmean = train.col.mean()\
> fstd = train.col.std()\
> train.ix\[np.abs(train.col-fmean) \> (3\*fstd), ‘col’\] = fmean + (3\*fstd) \# treat upper outliers\
> train.ix\[np.abs(train.col-fmean) \< -(3\*fstd), ‘col’\] = -(fmean + (3\*fstd)) \# treat lower outliers

-   **Univariate analysis**

> \# univariate analysis

> \# histogram of numerical column\
> plt.figure(figsize=(12,8))\
> sns.distplot(train\[“num”\].values, bins=10, kde=False)\
> plt.xlabel(‘num’, fontsize=12)\
> plt.title(“num histogram”, fontsize=14)\
> plt.show()

> \# charts of categorical column\
> labels = train.cat.unique()\
> sizes = \[train\[‘cat’\].value\_counts()\[1\],\
>  train\[‘cat’\].value\_counts()\[0\]\
>  \]\
> \# pie plot for categorical column\
> fig1, ax1 = plt.subplots()\
> ax1.pie(sizes, labels=labels, autopct=’%1.1f%%’, shadow=True)\
> ax1.axis(‘equal’)

> \# bar plot for categorical column\
> fig2, ax2 = plt.subplots()\
> sns.countplot(“col”, data=train)\
> plt.show()

-   **Bi-variate analysis**

> \# bivariate analysis

> sns.barplot(x=’cat1', y=’cat2', data=train) \# categorical vs categorical

> sns.violinplot(x=’cat’, y=’num’, data=train) \# categorical vs numerical

> sns.regplot(x=”num1", y=”num2", data=train) \# numerical vs numerical

-   **Multivariate analysis**

> \# multivariate analysis

> temp = train\[cols\_to\_use\]\
> corrmat = temp.corr(method=’spearman’)\
> f, ax = plt.subplots(figsize=(20, 20))

> sns.heatmap(corrmat, vmax=1., square=True, cmap=”YlGnBu”, annot=True)\
> plt.title(“numerical variables correlation map”, fontsize=15)\
> plt.show()

-   **Split data**

> \# split data

> y = train.target\
> X = train.drop(‘target’, axis=1, inplace=False)

> X\_train, X\_val, y\_train, y\_val = train\_test\_split(X, y,random\_state = 123)

-   **Feature engineering on train/valid**

> \# feature engineering on train/valid

> label = LabelEncoder()\
> X\_train\[‘cat’\] = label.fit\_transform(X\_train\[‘cat’\]) \# for categorical data

> scaler = MinMaxScaler() \# for numerical data\
> scaler.fit(X\_train) \
> X\_train = scaler.transform(X\_train)\
> X\_val = scaler.transform(X\_val)

-   **Build model on train**

> \# build model on train

> model = linear\_model.LogisticRegression(C=1e5) \# RandomForestClassifier(), SVC(), RandomForestRegressor() etc

> model.fit(X\_train, y\_train)

> y\_pred = model.predict(X\_val)

> model.score(X\_train, y\_train)

-   **Evaluate on valid**

> \# evaluate on valid

> confusion\_matrix(y\_val, y\_pred) \# for categorical target

> mean\_squared\_error(y\_true, y\_pred) \# for numerical target

-   **K-fold cross-validation**

> \# k-fold cross-validation

> model = svm.SVC(kernel=’linear’, C=1)

> scores = cross\_val\_score(model, X\_train, y\_train, cv=5)

> print(“Score: %0.2f (+/- %0.2f)” % (scores.mean(), scores.std() \* 2))

-   **Hyper-parameter tuning**

> for gamma in \[0.001, 0.01, 0.1, 1, 10, 100\]:\
>  for C in \[0.001, 0.01, 0.1, 1, 10, 100\]:\
>  \# for each combination of parameters,\
>  \# train an SVC\
>  svm = SVC(gamma=gamma, C=C)\
>  \# perform cross-validation\
>  scores = cross\_val\_score(svm, X\_train, y\_train, cv=5)\
>  \# compute mean cross-validation accuracy\
>  score = np.mean(scores)\
>  \# if we got a better score, store the score and parameters\
>  if score \> best\_score:\
>  best\_score = score\
>  best\_parameters = {‘C’: C, ‘gamma’: gamma}\
> \# rebuild a model on the combined training and validation set\
> svm = SVC(\*\*best\_parameters)\
> svm.fit(X\_train, y\_train)

------------------------------------------------------------------------

If you liked this post, have a look at another where I talk about ‘How to launch your DS/AI career in 12 weeks?’:

\[embed\]https://github.com/ankitrathi169/Data-Science-with-Python/blob/master/DataSciencePipeline.ipynb\[/embed\]

------------------------------------------------------------------------

*Thank you for reading my post. I regularly write about Data & Technology on* [*LinkedIn*](https://www.linkedin.com/today/posts/ankitrathi?source=post_page---------------------------) *&* [*Medium*](https://medium.com/@rathi.ankit?source=post_page---------------------------)*. If you would like to read my future posts then simply ‘Connect’ or ‘Follow’. Also, feel free to visit my webpage* [*https://ankitrathi.com*](https://www.ankitrathi.com/)*.*
