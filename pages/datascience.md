The data science process often begins with asking a simple question: What is happening?

Before any modeling or prediction can be done, a data scientist has to investigate using the data and tools available. 
We'll cover a variety of topics in this unit, starting with how to ask questions like a data scientist and what kind of questions a data scientist could answer. Next will be data accessing and aggregation with the querying language SQL, a key way of gathering data. Then we'll cover intermediate data visualization with an emphasis on data cleaning. Lastly we'll cover experimentation, a key way of using data to ask and answer questions.

As we consider how we want to define data science, it's useful to pull back a little bit to look at the larger picture. Data science does not exist in a vacuum. It doesn't exist on its own. Instead, it operates within a larger system. To understand its place within that system, then, it is worth understanding the architecture of that larger system.
#  The Technology Stack

When talking about a website or an app, people will often reference something called the stack or technology stack. This is the collection of elements that make up the given product. There is no single canonical 'stack,' and it will vary widely based on the application and the choices that engineers made when building it, though there are some common elements that a data scientist needs to be aware of.

First, let's talk about the front end. The front end is the the interface that users interact with: the website displayed in the browser or the mobile app on someone's phone. It is typically a combination of HTML, CSS, and JavaScript (as well as some JavaScript libraries like JQuery or React) in the case of a website or Swift in the case of an iOS app. Data scientists typically have limited interaction with front end engineering, though they could be working on experiments that include changes to the front end and the front end often plays a role in collecting data, so it is something to be familiar with.

The counterpart to the front end is, unsurprisingly, the back end. The back end can contain many different components, though some of the most common are servers, services, and the database. Servers run the applications of the website or app. Services are the code that actually generates or stores data from the app, among many other things (think about recording signup information a user puts into a form). And the database stores all of this information. If a data science model is deployed in production (say to offer personalization or intelligence to a process by ranking the results of a search or providing suggested videos on YouTube) that code will almost certainly exist in the back end.

Data science can also operate outside the production stack, and the development process where a model or system is initially designed and tested will typically happen outside of the production stack.

# So what is Data Science?
When trying to define what a data scientist is, it's tempting to go back to that tweet from Josh Willis (a data engineer) we referenced in the fundamentals course: "[A] Person who is better at statistics than any software engineer and better at software engineering than any statistician." There is some truth to that. D
 Data science operates at the intersection of statistics and engineering. Of course, it's worth noting more details on which skills this course is meant to impart.
 In this course we'll focus on learning from data. Specifically, we will focus on what happens after data is collected. How do you use that data to learn more about customers or events? How can that data inform decisions and make processes more efficient? You will learn not only the skills to access and manipulate data, but to build models that draw out information or provide intelligence to a process. As such we will cover analytics, experimentation, modeling, and machine learning.
 
# Related Roles

There are several roles related to data science, and it is not uncommon to see some overlap in skills. It is worth being familiar with the other roles data science skills can fall under so that you see the roles best suited to your skills.
Data Analyst

Typically, data analysts have the mathematical and statistical skill to look at data and draw conclusions or create reports. Very similar roles can fall under names like Business Intelligence Analyst. They interpret the information and perhaps suggest responses. Some people consider data analysts to be less experienced data scientists, without the full set of skills described above. There may be some coding skill in a language such as Python or R, but they are generally less sophisticated programmers than data scientists. Similarly, they may have some modeling background but not of the range a data scientist would. It is also not uncommon for data analysts to become data scientists after they develop more skills on the job.
Data Engineer

A data engineer is a master of gathering and storing data. They exist a step before data science, though often work in close collaboration. They create and manage the pipelines that take data out of a process and put it somewhere people (like data scientists) can use it. Accordingly, they interact with the front end and back end of the production system more directly. Database types and storage methods are within their domain, as are the pipelines that move data from one place to another. Typically they do not have as much an emphasis on interpretation or analysis as a data scientist will have.
Machine Learning Engineer

A machine learning engineer specializes in algorithms and modeling, typically with a more robust understanding of algorithm design and efficiency than the average data scientist. Data scientists typically rely on packages (like scikit-learn) for modeling as we will in this bootcamp. Machine learning engineers on the other hand often create bespoke models for deployment in the production environment using languages like C or Go (which are much more performant than Python), and usually have deep programming experience.

# A New and Evolving Field

While we have proposed a loose definition of "data scientist" and the responsibilities that we expect data scientists to fill, it is important to note that this is a new and evolving field. Practically, what that means is that there is no universally agreed definition of what exactly a data scientist is that everyone buys into. The expectations of what data scientists can do vary from person to person and company to company, sometimes significantly. When you get into your career search don't feel bound by job titles. Judge job opportunities by their skills and requirements, rather than job title alone, to find positions that align with your interests.

# The data science toolkit
Data scientists frequently use a specified set of tools and programs to do their job. The tools of the trade are frequently referred to as the data science toolkit. We'll cover all the elements in further detail throughout the course, but it's worth taking a moment now to outline what those tools are and when they're used in practice.
Python

Python is at the center of almost everything we'll do and represents the core programming language for this course. Even when we're not working in Python, it will often be in order to get data into or out of a Python environment. This is also where most of the 'data science' will happen. Most analytical work will be in Python and modeling will also be done with this.

There are other programming languages that can be used for data science. R is probably the most common alternative, and there are certainly advantages to each language. R has some more developed statistical packages and a wider range of statistical tests and models readily available. Python, however, is a generally more robust programming language and used for a wider variety of tasks than just data science. You can take a Python project and seamlessly integrate it into larger infrastructure. That infrastructure may even be in Python itself. R is used almost exclusively for data work, so it doesn't have that broader range of functionality.

Packages

We'll expand the functionality of Python beyond its core library with a variety of packages. What follows is a non-exhaustive list of some of the packages we'll use and their purposes.

    [NumPy](https://en.wikipedia.org/wiki/NumPy#History) - The basic package for mathematical manipulation within Python.
    [Pandas](https://en.wikipedia.org/wiki/Pandas_%28software%29#History) - Contains the dataframe, which is the key data structure for data science. Built on top of NumPy.
    [matplotlib](https://en.wikipedia.org/wiki/Matplotlib) - Fundamental plotting library.
    [Seaborn](http://seaborn.pydata.org/) - A more sophisticated plotting library based on matplotlib.
    [scikit-learn](http://scikit-learn.org/stable/) - The core modeling and machine learning library in Python, with built-in tools for the majority of models we'll use.
    [StatsModels](http://www.statsmodels.org/stable/index.html) - An alternative modeling library.
    
Don't worry if you're not familiar with all of these packages yet (we'd be surprised if you were). We'll continue to go through them during the course. This may be a useful list to reference when working on projects and you're wondering where to look for certain functions. There is also a near infinite number of more specialized packages for more specific scenarios. The list really does go
[on and on and on.](https://pypi.org/)

SQL

Data will not always be available in an easy to use form. Sometimes there's just too much of it. Often it needs to be stored in a database for operational reasons. SQL ("Structured Query Language") is the way you get data out of most databases (like PostgreSQL, MySQL, Oracle, Microsoft SQL Server, Amazon's SimpleDB, and SQLite). We'll use SQL to access and preprocess data so that you're comfortable working with and extracting from databases when dealing with them professionally. HiveQL is the Hive version of SQL, which we will also cover in the Big Data section.

And that's it. There is a universe of specialized tools for particular domains, and you'll have a chance to dig into some of those later in the course, but these are the core tools of data science.

# Thinking like a data scientist
As a data scientist, your ability to think scientifically will set you apart from the code-ninja-unicorns and number-crunchers who otherwise share many of your skills. 
Curiosity is something we're all born with. It's the engine behind "Why" and "How" questions, the desire to get behind the scenes, to know more than what we can see or understand right now. Curiosity leads to questions, and answering questions is data science's raison d'être, the reason the career exists. 
Of course, not all questions can be answered with data, and some can't be answered at all. A skilled data scientist makes sure to define their questions in ways that are amenable to data-oriented solutions – this is where practicality comes in. "What is the meaning of life?" is not a question that can be answered with data. "What do people believe about the meaning of life?", on the other hand, is a practical question that falls squarely in the data scientist's realm.
Finally, a data scientist is skeptical. They not only describe what seems to be happening in a dataset but also how much confidence we can place in the results we see. The conclusions from a dataset will always be limited in various ways, from noisy data to unusual samples, and data scientists take those limitations into account when presenting their findings.

Making real-life questions testable

As a rule of thumb, questions that can be answered with a number or numbers can be addressed by a data scientist. For example, 56% of people might say the meaning of life is "42", or analysis of Facebook statuses might find 1000 different discussions mentioning the meaning of life in the last 24 hours.
Even if a question doesn't seem like it has a numeric answer, it can often be rephrased in a way that makes it answerable with data. For example, "Why do bad things happen to good people?" is a compelling question that has been debated for thousands of years. A data scientist might contribute to the conversation by breaking the question down in the following ways:

    Providing a concrete definition of "bad things," such as "being the victim of a crime."
    Providing a concrete definition of "good people," such as "people who volunteer once a month or more."
    Collecting data, or finding an existing dataset, containing data from people who were and were not victims of crimes, and do and do not volunteer once a month or more. This creates four quadrants, or buckets. For example:

     

	Volunteer >= once a month 	Volunteer < once a month
Victim of a crime 	- 	-
Not victim of a crime 	- 	-

    Fill the buckets with data. The "good people, bad things" quadrant is top left.

	Volunteer >= once a month 	Volunteer < once a month
Victim of a crime 	60% female
71% urban
Mean age 44
Mean yearly income $35,000
1.5 kids 	50% female
67% urban
Mean age 32
Mean yearly income $58,000
1.6 kids
Not victim of a crime 	55% female
39% urban
Mean age 47
Mean yearly income $34,000
1.4 kids 	40% female
32% urban
Mean age 34
Mean yearly income $56,000
1.7 kids

    Look for combinations of characteristics that are unique to the "good people, bad things" quadrant.

	Volunteer >= once a month 	Volunteer < once a month
Victim of a crime 	60% female
Mean yearly income $35,000
71% urban 	50% female
Mean yearly income $58,000
67% urban
Not victim of a crime 	55% female
Mean yearly income $34,000
39% urban 	40% female
Mean yearly income $56,000
32% urban

Our quadrant of people who volunteer more than once a month and are victims of crime are more likely to be women than any other quadrant. In addition, they have a unique combination of low income and high likelihood of living in a city. So we might tentatively conclude that "bad things happen to good people" because these people are more likely to also be poorer women who live in a city, a combination of variables that increases their risk.

Are there flaws in this approach? Of course! We don't know what is causing poorer women who live in a city to be more likely to volunteer and be victims of crime, we just know the characteristics are associated with each other. In addition, people might take issue with our variable definitions. 
They may argue that being a "good person" isn't (just) about volunteering, or that the category of "bad things" is much broader than just being victimized by crime. And they would be right. In translating the big question "Why do bad things happen to good people?" into something data science can tackle, we've lost a great deal of information and nuance. On the other hand, we've also learned something, perhaps laying the groundwork for a follow-up project. Lastly, note that we have to balance between trying to answer as much as possible with having confidence in our conclusions. Learning to ask a question that is significantly broad to be relevant but precise enough to be solvable is another aspect of this same skill.

Sometimes the way a question is translated is dictated by the data available. If a company wants to learn about the mental health of their employees, but the only data they have is a question about job satisfaction within a larger employee survey, then they can either decide that "satisfied with my job" can stand in for "mentally healthy," or they can spend the money and time to collect new data.

Finding and evaluating data sources

Data is everywhere. The trick is to know where to look to find data that is relevant to our research questions. Data sources range from archives with carefully curated databanks full of information to the flood of information poured out every day on Twitter, Facebook, and the rest of the web. Unless you're an experienced web-scraper, we recommend sourcing the data for course projects from data archives 
and [repositories like these](https://github.com/Thinkful-Ed/data-201-resources/blob/master/data-sources.md). 

Not all datasets are created equal. We recommend datasets supplemented with meta-data (data about data), including when and where the data was collected, what the population of interest was, the sampling technique used, and information about the individual variables. Meta-data may be available as a webpage, an additional data file, or (depending on the file format used) information embedded within the main datafile. 

The dataset must also be available in a database or readable file format. Fortunately, the pandas package provides 
support for [most widely-used file formats](http://pandas.pydata.org/pandas-docs/stable/io.html), and you learned about accessing CSV, JSON, and XML files in the fundamentals course. 

# Evaluating uncertainty

[It is easy to overstate the informative value of a statistic](http://phdcomics.com/comics/archive.php?comicid=1174) 
. Most people aren't used to looking at a number and wondering about the process that made it. One of the services a data scientist provides is to assess how certain we can be that conclusions based on a particular statistic are valid. Sources of uncertainty include the source of the sample, the size of the sample, 
and the [amount of noise (variance) in the data](https://velica.deviantart.com/art/Error-bars-101948712). 

Sampling a homogenous population, such as college students, leads to uncertainty when generalizing to other populations, such as working adults.

As you saw earlier, smaller samples lead to larger standard errors and wider margins of error. An election poll might project a 3% lead for candidate A, with a margin of error of plus or minus 5, meaning the true lead for candidate A could be anywhere from 8% to -2% (losing to candidate B). A larger sample would shrink that margin of error.

Noisy data is more difficult to summarize. Two different variables can be described with a mean of 30, but if Variable 1 has a range of values from 25 to 40 and Variable 2 has a range of values from -30 to 90, then the mean of Variable 1 tells us a lot more about the datapoints in Variable 1 than the mean of Variable 2 does for the datapoints in Variable 2.

# Translating statistical results into plain English
When reporting the results of statistics it is easy to lapse into jargon, specialized language like "variance" or "bimodal" that exactly describes your results 
but that may be [opaque to others](http://www.savagechickens.com/2009/03/love-stats.html). Keep in mind your intended audience, and always ground your findings in the question you're trying to answer. 



For example, instead of saying "Group 1 had a higher mean but lower variance than Group 2, while Group 2 had some left-leaning skewness," try "Web customers spent more than app customers, but app customers differed more among one another in how much they spent, with some spending as little as $.50 per visit."
