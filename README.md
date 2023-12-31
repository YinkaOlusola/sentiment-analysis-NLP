# Sentiment Analysis Project using Natural Language Processing.
## Planet Solver - A Product Pitch by Emerald; a team of Data Scientists
Many companies are built around lessening environmental impact or carbon footprint. They offer products 
and services that are environmentally friendly and sustainable, in line with their values and ideals.

Emerald, a team of Data Scientists in this project pitched a product that can help companies to determine 
how people perceive climate change and whether or not they believe it is a real threat. This would add 
to their market research efforts in gauging how their product/service may be received.

<br>

## Task
Emerald was challenged in the Classification Sprint with the task of creating a Machine Learning model 
that is able to classify whether or not a person believes in climate change,  based on their novel tweet data.

<br>

## Objective
Providing an accurate and robust solution to this task gives companies access to a broad base of consumer 
sentiment, spanning multiple demographic and geographic categories - thus increasing their insights and 
informing future marketing strategies.

<br>

## Data

The collection of this data was funded by a Canada Foundation for Innovation JELF Grant to Chris Bauch, University of Waterloo. The dataset aggregates tweets pertaining to climate change collected between Apr 27, 2015 and Feb 21, 2018. In total, 43943 tweets were collected. Each tweet is labelled as one of the following classes:

**Class Description**

 - 2 News: the tweet links to factual news about climate change
 - 1 Pro: the tweet supports the belief of man-made climate change
 - 0 Neutral: the tweet neither supports nor refutes the belief of man-made climate change
 - -1 Anti: the tweet does not believe in man-made climate change

**Variable definitions**

 - sentiment: Sentiment of tweet
 - message: Tweet body
 - tweetid: Twitter unique id

<br>

## Exploratory Data Analysis

- Data Cleaning and Exploratory Data Analysis (EDA): The Data was cleaned and important visualizations about the available data were carried out.

Based on the data set used in the project, below is the tweet distribution with class Pro having a very high frequency.

<br>

**Tweet Distribution**
<img src="resources/plot_images/tweet_distn.png" alt="Tweet distribution" width ="800" height="400">

<br>

A close look at the above distribution indicates that the data is severely imbalanced with the majority	of tweets falling in the 'pro' category, supporting the belief of man-made climate change while just 6% are anti-climate change

<br>

**Tweet per class**
<img src="resources/plot_images/length_of_tweet_per_class.png" alt="Length of Tweets per class" width ="800" height="400">


From the boxplot, it could be observed that tweets that fall in the pro climate change class are generally longer and the shortest tweets belong to the anti climate change class.

This can be seen from the respective spans of the plots. It seems that we have strong-witted pros here!!

It is worthy to also note that neutral climate change tweets tend to have the most variability in tweet length


### Top Hashtags

Hashtags being a powerful feature used in sorting and organizing tweets provide an excellent approach to show that a content is related to a specific issue.

It could be helpful in unraveling what the most popular hashtags are in each of the classes which would help in obtaining a better grasp of the types of knowledge ingested and shared by members of each class.

<br>

**Top Hashtags for Pro Climate Change**
<img src="resources/plot_images/top_hashtags_pro_climate_change.png" alt="Top Hashtags for Pro Climate Change" width ="600" height="300">

<br>

**Top Hashtags for Anti Climate Change**
<img src="resources/plot_images/top_hashtags_anti_climate_change.png" alt="Top Hashtags for Anti Climate Change" width ="600" height="300">

<br>

**Top Hashtags for News on Climate Change**
<img src="resources/plot_images/top_hashtags_news_class.png" alt="Top Hashtags for News on Climate Change" width ="600" height="300">

<br>

**Top Hashtags for Neutral Tweets on Climate Change**
<img src="resources/plot_images/top_hashtags_neutral_class.png" alt="Top Hashtags for Neutral tweets on Climate Change" width ="600" height="300">



Knowing the popular words used across various classes can help to understand how customers think or are thinking.

## Model Training and Evaluation

Various machine learning models were trained on the dataset and performance of the models were tracked and recorded using Comet.

The evaluation metric for the Kaggle competition was Weighted F1-score Prediction of an individual's climate change sentiment class is commonly used in classifications problems.

After comparison of the different models, the support vector classifier (SVC) was selected as it gave the best performance among the tested models using the F1-score as shown below.


**Model Performance comparison**
<img src="resources/plot_images/models_performance_comparison.JPG" alt="Image Description" width ="600" height="300">

<br>

## Kaggle Submission

The random forest model was used to make a submission on Kaggle for the [Climate Change Belief Analysis Challenge](https://www.kaggle.com/competitions/edsa-climate-change-belief-analysis-2022/leaderboard) where my team was able to attain an 8th position on the leaderboard after a lot of fine-tuning of the model.


- Machine Learning Model training: Different machine learning models were considered; Logistic Regression,
  Support Vector Classifier, Random forest classifier, Naive Bayes classifier, and K Nearest Neighbour classification.

- Model Performance: This was tracked using Comet, a web-based platform used for keeping records of machine learning model performance.
  The model with the best performance, SVC, was selected and used to make predictions that were used for the Kaggle competition.

- Recommendations: These were made based on the result of the project.

## Streamlit

Streamlit is an open-source app framework in Python language that is used to create web apps for data science and machine learning in a short time. 

The [Streamlit web application](https://sentiment-analysis-on-climate-change.streamlit.app/)

A video demo of the Streamlit app being used is at [Web app video demo](https://drive.google.com/file/d/1eweMv369ICT-a3ZN4E6qsE9UxlBDqlFs/view?usp=drive_link)

## The Pitch.
The Product was pitched to a panel of stakeholders and the pitch presentation is at [Product Pitch](https://www.canva.com/design/DAFDvHeY0N8/gEwp_FiznbPwkxQt7uqGSQ/edit?utm_content=DAFDvHeY0N8&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton).
