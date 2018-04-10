# Day 1
The goal of this course is to provide an end-to-end blueprint for applied machine learning, while keeping this as actionable and succinct as possible.This course starts with a bird's-eye view of applied machine learning, clearing up some common misconceptions and explain how to succeed in this field.  Then, it spend some time on critical (yet often overlooked) steps such as exploratory analysis, data cleaning, and feature engineering. Only after this introduction, effective ML algorithms and exactly how to train professional-grade models will be discussed, while sharing current industry best practices. The final part of this crash course will provide a step-by-step action plan for building real-world skills that will open exciting career opportunities.

Here’s the recommendations for making the most out of this crash course: 

  1. Keep up: Each lesson is concise so it can fit any schedule. However, because the lessons build on each other, staying on schedule helps solidify the concepts.
  2. Don’t sweat the details for now: Students master this subject faster by first understanding how all the pieces fit together and only then diving deeper. This trainings follow this “top-down” approach.
  3. Don’t worry about coding yet: It’s easy to get lost in the weeds at the beginnin, so try to see the forest instead of the trees. The code will come later.

## [Bird's Eye View](https://elitedatascience.com/birds-eye-view)
Let's start by training your first machine learning model using this [step-by-step tutorial](https://elitedatascience.com/python-machine-learning-tutorial-scikit-learn) for training a model that can predict wine quality. Tutorials like this are excellent for getting your feet wet, but to consistently get great results with machine learning, it is important to develop a reliable, systematic approach to solving problems. And that's what the rest of this course will tackle.

### Introduction
First, one of the biggest misconceptions about machine learning is that it is all about algorithms. This is because, 
all textbook or university syllabus are organized as a grocery list of algorithm, fuelling the misconception that machine learning is about mastering dozens of algorithms. However, **Machine learning is a comprehensive approach to solving problems and individual algorithms are only one piece of the puzzle**. The rest of the puzzle is how to apply them the right way.

### What makes machine learning so special?
Machine learning (ML) is the practice of teaching computers how to learn patterns from data, often for making decisions or predictions, without being explicitly programmed to identify these patterns. So, in machine learning, the patterns that the computer finds are not hard coded, with only the "guidelines" of how to look for the patterns being coded.

### Key Terminology
It is important to be clear and concise with our terminology, making sure that a shared language is used. Important terms for machine laerning include: 

  * **Model**: a set of patterns learned from data.
  * **Algorithm**: a specific ML process used to train a model.
  * **Training data**: the dataset from which the algorithm learns the model.
  * **Test data**: a new dataset for reliably evaluating model performance.
  * **Features**: variables (columns) in the dataset used to train the model.
  * **Target variable**:a specific variable you're trying to predict.
  * **Observations**: data points (rows) in the dataset.

### Machine Learning Tasks

Academic machine learning starts with and focuses on individual algorithms. However, in applied machine learning, picking the  right machine learning task for the job is the first step A task is a specific objective for which many algorithms can be used. As such, ML algorithms can often be swapped fro the same taks. In fact, it is always a good idea to try multiple algorithms because it is difficult to know which one will perform best *a priori*. The two most common categories of tasks are supervised learning and unsupervised learning. **Supervised learning** includes tasks for "labeled" data (defined target variable). In practice, it's often used as an advanced form of predictive modeling, where each observation must be labeled with a "correct answer". Only then can a predictive model be build because the algorithm needs to know what is "correct" while training it (hence, being "supervised"). Two supervised learning tasks include **Regression**, for modeling continuous target variables, and **Classification**, for modeling categorical ("class") target variables. **Unsupervised learning** includes tasks for "unlabeled" data (no defined target variable). In practice, it's often used either as a form of automated data analysis or automated signal extraction, where unlabeled data has no predetermined "correct answer". The the algorithm will directly learn patterns from the data (without "supervision"). **Clustering**, for finding groups within your data, is the most common unsupervised learning task.

### The 3 Elements of Great Machine Learning
*How to consistently build effective models that get great results*

   1. A skilled chef (human guidance): there are dozens of decisions to be made along the way that go beyond running the learning algorithm. The very first major decision is how to road-map the project for guaranteed success.
   
   2. Fresh ingredients (clean, relevant data): the quality of the data is an essential element (*Garbage In = Garbage Out*). No matter which algorithm is used, professional data scientists spend most their time understanding the data, cleaning it, and engineering new features. 
   
   3. Don't overcook it (avoid overfitting): One of the most dangerous pitfalls in machine learning is overfitting. An overfit model has "memorized" the noise in the training set, instead of learning the true underlying patterns. Overfitting is still the single largest mistake to avoid. Strategies for preventing overfitting include choosing the right algorithms and tuning them correctly.
   
### The Blueprint

Machine learning should not be haphazard and piecemeal. It should be systematic and organized. 
The machine learning blueprint is designed around the 3 previous elements and is organized arounf 5 core steps:

  1. Exploratory Analysis: First, "get to know" the data. This step should be quick, efficient, and decisive.
  2. Data Cleaning: Then, clean your data to avoid many common pitfalls. Better data beats fancier algorithms.
  3. Feature Engineering: Next, help the algorithm "focus" on what's important by creating new features.
  4. Algorithm Selection: Choose the best, most appropriate algorithms without wasting time.
  5. Model Training: Finally, train the model. This step is pretty formulaic once you've done the first 4.

Of course, there are other situational steps as well, which can be easily picked up once the core workflow is understood.

  * Project Scoping: Sometimes, the project needs to be roadmaped and data needs anticipated.
  * Data Wrangling: Restructure of the dataset into a format that algorithms can handle may be required.
  * Preprocessing: Often, transforming the features first can further improve performance.
  * Ensembling: Even more performance can be squeezed out by combining multiple models.

### Additional Resources

[9 Mistakes to Avoid When Starting Your Career in Data Science](https://elitedatascience.com/beginner-mistakes)
[Free Data Science Resources for Beginners](https://elitedatascience.com/data-science-resources)

# Day 2 
There’s a big challenge in data science that we must address and it’s called “Tactical Hell”. 
This is actually a term from startups, and it’s when there are have too many tactics to choose from. 
In many ways, training a ML model is like growing a startup. There are too many tactics to choose from, a lot of trial and error and figuring it out along the way! This is the topic of today’s lesson: how do you avoid wasting time chasing dead ends?

## [Exploratory Analysis](https://elitedatascience.com/exploratory-analysis)

This lesson dives into the first step of the core machine learning workflow: Exploratory Analysis.a fancy term for “getting to know” the data. Doing this upfront is the best way to save time and avoid wild goose chases. Exploratory analysis is like sending your scouts ahead to learn where best to deploy your forces!

###  Introduction
The purpose of exploratory analysis is to "get to know" the dataset. Doing so upfront will make the rest of the project much smoother, in 3 main ways:

  1. Gaining valuable hints for Data Cleaning (which can make or break your models).
  2. Thinking of ideas for Feature Engineering (which can take your models from good to great).
  3. Gettting a "feel" for the dataset, which will help you communicate results and deliver greater impact.

However, exploratory analysis for machine learning should be quick, efficient, and decisive. 
There are infinite possible plots, charts, and tables, but only a handful are needed to "get to know" the data well enough to work with it.Don’t skip this step, but don’t get stuck on it either.

### Basic information
Exploratory analysis starts by answering a set of basic questions about the dataset. It is important to display example observations from the dataset to get a "feel" for the values of each feature and check if everything makes sense. The purpose of displaying examples from the dataset is not to perform rigorous analysis but to get a qualitative "feel" for the dataset based on a quick eyeball test.

  * How many observations and features are there? 
  * What are the features numeric or categorical? 
  * Is there a target variable?
  * Do the observations and their values make sense? 
  * Are the values on the right scale?
  * Is missing data going to be a big problem?

### Distributions of numeric features
It can be very enlightening to plot the distributions of your numeric features.
Often, a quick and dirty grid of histograms is enough to understand the distributions.

  * Distributions that are unexpected
  * Potential outliers that don't make sense
  * Features that should be binary (i.e. "wannabe indicator variables")
  * Boundaries that don't make sense
  * Potential measurement errors

At this point, it is important to make notes about potential fixes for the Data Cleaning step. If something looks out of place, such as a potential outlier in one of your features, now is a good time to ask the client/key stakeholder, or to dig a bit deeper.

### Distributions of categorical features

Categorical features cannot be visualized through histograms and are instead visualized with bar plots. These plots allow to quickly check the feature classes, that is, the possible unique values for a given categorical feature. In particular, look out for sparse classes, which are classes that have a very small number of observations. These classes tend to be problematic when building models. They don't influence the model much but they may, in the worse case, cause the model to be overfit. 
Take note to combine or reassign (maybe create a *others* class) some of these classes when doing the Feature Engineering.

### Segmentations

Segmentations are powerful ways to observe the relationship between categorical features and numeric features and 
can be done easily with Box plots. These provide a number of insights about the data. 

  * Are the median values (middle vertical bar in the box) different between class.
  * Are the min and max values different between the two classes.
  * Are there any possible data truncation? Are the min and max value limited round-numbers? Data truncation can affect model generalizability.

### Correlations

Finally, correlations allow to find the relationships between numeric features. Correlation is a value between -1 and 1 that represents how closely two features move in unison. Positive correlation means that as one feature increases, the other increases, while a negative correlation means that as one feature increases, the other decreases. Correlations of -1 or 1 indicate a perfect relationship and correlation of 0 indicates no relationship. Correlation heatmaps help to visualize this information and to look for

  * Which features are strongly correlated with the target variable?
  * Are there interesting or unexpected strong correlations between other features?

### Conclusion

Again, the aim is to gain intuition about the data, which will help throughout the rest of the workflow.
By the end of your Exploratory Analysis step, there should be a pretty good understanding of the dataset, some notes for data cleaning, and possibly some ideas for feature engineering.

### Additional Resources
[Data Visualization with Python's Seaborn Library](https://elitedatascience.com/python-seaborn-tutorial)

# Day 3
Proper data cleaning is a bit boring, so no one really talks about it. But the truth is that *garbage in gets you garbage out*, plain and simple! With a clean dataset, even simple algorithms can learn impressive insights from it! Different problems will require different methods but, for now, let’s at least ensure we know how to fix the most common issues.

## [Data Cleaning](https://elitedatascience.com/data-cleaning)
With the dataset "explored", it's time to get it into tip-top shape.
 
### Introduction
Proper data cleaning can make or break a project. Professional data scientists usually spend a very large portion of their time on this step because of a simple truth in machine learning: Better data beats fancier algorithms. Obviously, different types of data will require different types of cleaning. However, the systematic approach laid out in this lesson can always serve as a good starting point.

### Unwanted observations

The first step to data cleaning is removing unwanted observations from your dataset. This includes duplicate or irrelevant observations. **Duplicate observations** most frequently arise during data collection, such as when datasets are combined from multiple places, data is scraped or received from clients/other departments. **Irrelevant observations** are those that don’t actually fit the specific problem that you’re trying to solve. This includes data for variables or categories that were collected but are not related to the problem. This is also a great time to review the charts from Exploratory Analysis and look at the distribution for categorical features to see if there are any classes that shouldn’t be there. For example, if you were building a model for Single-Family homes only, you wouldn't want observations for Apartments in there. Checking for irrelevant observations before engineering features can save you many headaches down the road.

### Structural errors

Structural errors are those that arise during measurement, data transfer, or other types of "poor housekeeping", including typos or inconsistent capitalization. This is mostly a concern for categorical features, so review the bar plots from the Exploratory analysis to confirm there are no naming issues with the categorical values such as having simultaneously the classes *composition* and  *Composition* or *composition .* After correction typos and inconsistent capitalization, the class distribution becomes much cleaner. Finally, check for mislabeled classes, such as separate classes that should really be the same. For example, *N/A* and *Not Applicable* should be combined.

### Unwanted outliers

Outliers can cause problems with certain types of models such as linear regression models, which are less robust to outliers than decision tree models. In general, **if there is a legitimate reason** to remove an outlier, it will help the model’s performance. However, outliers are innocent until proven guilty and should never be removed just because it’s a "big number." That big number could be very informative for your model. Tehre **has** to be a good reason for removing an outlier, such as suspicious measurements that are unlikely to be real data.

### Missing data
Missing data is a deceptively tricky issue in applied machine learning. Missing values cannot simply br ignored. They must handled in some way for the very practical reason that most algorithms do not accept missing values.

"Common sense" is not sensible here. Unfortunately, from our experience, the 2 most commonly recommended ways of dealing with missing data actually suck. These are dropping observations that have missing values and imputing the missing values based on other observations. **Dropping missing values** is sub-optimal because when you drop observations, you drop information. Not only the fact that the value was missing may be informative in itself, in the real world, it is often required to make predictions on new data even if some of the features are missing! **Imputing missing values** is sub-optimal because the value was originally missing but you filled it in, which always leads to a loss in information, no matter how sophisticated your imputation method is.
Again, "missingness" is almost always informative in itself, and you should tell your algorithm if a value was missing and imputing values, does not addi any real information, it simply reinforces the patterns already provided by other observations.
In short, **always tell the algorithm that a value was missing because missingness is informative**. 


Missing categorical data

The best way to handle missing data for categorical features is to simply label them as ’Missing’!

    You’re essentially adding a new class for the feature.
    This tells the algorithm that the value was missing.
    This also gets around the technical requirement for no missing values.


Missing numeric data

For missing numeric data, you should flag and fill the values.

    Flag the observation with an indicator variable of missingness.
    Then, fill the original missing value with 0 just to meet the technical requirement of no missing values.

By using this technique of flagging and filling, you are essentially allowing the algorithm to estimate the optimal constant for missingness, instead of just filling it in with the mean.


### Conclusion

After properly completing the Data Cleaning step, the resulting dataset should be robust and avoids many of the most common pitfalls.This can really save a ton of headaches down the road, so  don't rush this step.

### Additional Resources

[How to Handle Imbalanced Classes in Machine Learning](elitedatascience.com/imbalanced-classes)
[Datasets for Data Science and Machine Learning](https://elitedatascience.com/datasets)

# Day 4
Pretty nice, let's keep going...

...lots of great stuff to get to in the second half!

Yesterday, you learned a reliable framework for cleaning your dataset…

Today, in day 4 of our 7-day crash course, we're going to discuss “feature engineering.”

In a nutshell, feature engineering is the process of creating new features from your existing ones.

That doesn’t sounds like much…

…Yet Andrew Ng, former head of Baidu AI and Google Brain, said:

“Coming up with features is difficult, time-consuming, requires expert knowledge.
‘Applied machine learning’ is basically feature engineering.”

Wow!

Absolutely no pressure, right?

So why is it so difficult and time-consuming?

To start, feature engineering is very open-ended. There are literally infinite options for new features to create.

Plus, you’ll need domain knowledge to add informative features instead of just more noise.

This is a skill that you’ll develop naturally with time and practice, but you can give yourself a big head-start if you have a framework in place.

A feature engineering framework simply consists of "heuristics" that you can rely on to spark ideas.

If you're a beginner, heuristics can help you know where to start looking... and if you're experienced, heuristics can help you get unstuck.

In today’s lesson, we’ve compiled our favorites:
[Go to Lesson 4: Feature Engineering](https://elitedatascience.com/feature-engineering)

# Day 5
Yesterday, you learned several different heuristics to inspire ideas for feature engineering.

Today, we're going to dive into Algorithm Selection.

In this lesson, we'll introduce 5 very effective machine learning algorithms for regression.

They each have classification counterparts as well.

And yes, just 5 for now!

Instead of giving you a long list of algorithms...

...our goal is to explain a few essential concepts (e.g. regularization, ensembling, automatic feature selection) that will teach you why some algorithms tend to perform better than others.

In applied machine learning, individual algorithms should be swapped in and out depending on which performs best for the problem and the dataset.

Therefore, we will focus on intuition and practical benefits over math and theory.

We have two main goals for this lesson:

    To Introduce Powerful Mechanisms in Modern Machine Learning
    To Tour Several Algorithms That Use Those Mechanisms.

So if you're ready to jump on this, click the link below now:
[Go to Lesson 5: Algorithm Selection](https://elitedatascience.com/algorithm-selection)

# Day 6

Yesterday, we introduced 5 algorithms and their underlying mechanisms.

Today, we'll look at how to systematically train effective models.

Yes, this is what you’ve been waiting for...

...at last...

...it’s time to build our models.

It might seem like it took us a while to get here...

...but professional data scientists actually spend the bulk of their time on the steps leading up to this one:

    Exploring the data.
    Cleaning the data.
    Engineering new features.

Again, that’s because better data beats fancier algorithms.

In this lesson...

...you'll learn how to maximize model performance while safeguarding against overfitting.

Plus, you'll learn how to automatically find the best parameters for each algorithm.

We'll walk through an overview of each of these steps:

    Split dataset
    Decide on hyperparameters
    Set up cross-validation
    Fit and tune models
    And finally...Select a winner!

See you inside the lesson:
[Go to Lesson 6: Model Training](https://elitedatascience.com/model-training)

# Day 7
This is the very last day of the crash course!

We've got a very special final installment especially for you.

BTW, Nice job following along so far... we've really covered a lot of ground over the last week!

    On day 1, you saw a bird's-eye view of the entire machine learning workflow.
    Then, on day 2, you learned our framework for fast, efficient, and decisive exploratory analysis.
    Day 3 was all about data cleaning, which is perhaps the most important step of all!
    Next, on day 4, we shared our favorite heuristics for feature engineering.
    On day 5, we discussed regularization and ensembles, and you learned about 5 algorithms that leverage those mechanisms.
    And yesterday on day 6, we walked through a proven formula for training excellent models after the other steps have been completed correctly.

(Links all the lessons are included at the start of today's lesson)

Now, we'll give you our best recommendations for where to go from here...
 
...including how to transform these concepts into invaluable, practical skills that can significantly impact your career.
[Go to Lesson 7: Next Steps](https://elitedatascience.com/next-steps)
