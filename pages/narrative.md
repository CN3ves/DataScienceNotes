# Narrative Analytics

Narrative analytics is the idea of telling a story with data, and it will play a key role in everything you do in this course and throughout your career in data science. As we explore this concept in this lesson, it's important to acknowledge that the job of a data scientist is not always narrative.

Particularly when dealing with technical coworkers, sometimes the job of a data scientist is to just gather and present information with as little influence on the process as possible. This is a more passive form of data science, focused almost solely on the integrity of the data.

However, we will by and large not emphasize that kind of data science, for a few reasons. Firstly, the skills for passive analytics (the math, stats, data collection) are still necessary for narrative analytics. Adding a narrative just puts another layer on top of that work. Secondly, learning the narrative form and how to make a case with data is a difficult skill to master, requiring constant practice and reinforcement. Lastly, adding a narrative is often a key value add of a data scientist. How so? We'll explore that below.
Everything is a story...

As much as we acknowledge it above as a valid approach to data science, there's really no such thing as truly passive data science. Everything contains some element of narrative to it. Every piece of data says something, and how you present those points inherently affects how such data is consumed. Understanding how that happens is key to being a successful data scientist.

Let's start with a simple example.

Let's say you work at a furniture store and sales for last week were $20,502.

That is a piece of data operating in a relatively minimal amount of context. Perhaps to the furniture store owner, who has experience and context, they can take that piece of information and put it into some kind of understanding of whether those sales were good or bad, up or down, expected or anomalous. However, with just that single piece of data none of that other information is conveyed. The story is short, and it is largely left to the person consuming the data to fill in the narrative around it.

Now let's think of another way we could talk about sales: "Sales last week were $20,502, down 1% over the previous week."

This provides a little more context, but while this may seem dispassionate, there are several choices that were made here that will shape interpretation. Firstly, it only looks back a single week. It doesn't tell us anything about any larger trend that exists or put it into the context of how much volatility we typically see in sales.

If we compared against average sales for the past year, we might see something like sales that week as 10% above the mean. Is that a more descriptive metric? It certainly makes it sound like sales were good. But is the trend improving or leveling off?
Answers are always a partial picture

Any time you answer a question about data you're inherently summarizing the data. That means something is going to be lost. It's unavoidable. Any interpretation is a version of taking a stance about what the data means.

As a data scientist, your job is not to tell the whole story but to tell the best one you can with the information you have at hand. Sometimes it's to argue for a specific reaction. Sometimes it's to present a certain version of events. If you think sales are weak you're probably not going to compare to last year's average.

Recognize that any way you present your data presents a version of events. It's not that one version is true or one is false. It's that they're different. That's why asking the right question, and not just that but asking a lot of questions, is essential to finding out what is going on with your data.
Aren't we supposed to be dispassionate?

There's a mistrust around data that it is manipulable. A really talented statistician or data scientist can find ways to present the same dataset to tell contradicting stories. Does that mean any of our work can be dispassionate or done with integrity?

Of course it can.

There are several key things to keep in mind when working with data to ensure that you arrive at the closest thing to truth you can find.

Firstly, try not to decide a story before you look into the data. The analysis you perform should inform the narrative you want to tell, not the other way around.

Always try to ask what else an answer could mean. When you perform analytics, there is often a conclusion that is easiest to draw. Seeing that sales had a down week could easily mean that sales are in trouble. Spending the time to question that conclusion is one of the key features of a good data scientist.

Lastly, be aware that you can always be wrong. Conclusions aren't 100%. There's never just one interpretation. Keep questioning what's going on. Keep asking more questions.

Remain curious.

Always.

# What Makes a Good Visual

Now, when we talk about the analysis we perform, there are two main things we present. First is numeric summarization and analytics. These are the kinds of things we talked about previously. Statistical tests, measures of central tendency. Those kinds of things.

Then there are visualizations.

Being able to make good visualizations is one of the most valuable skills a data scientist can possess. It is remarkable how often all the statistics and analytics are done and lined up making a compelling statistical case, but people do not buy into it until they see the visualizations.
Visuals as narrative device

Just like summary statistics, visualizations are a narrative device in your analytic reporting. We're going to continue with the sales example from the previous lesson.

Base Image

Here we have a plot of sales over time, specifically a line graph, which we covered earlier in the prep course. However, this is not a very good plot. The axes are unlabeled. There's no title. We really know nothing about the plot other than something seems to be going up and to the right.

Why does this matter if you know we're talking about sales? There is a simple fact worth remembering when doing analytic reporting: most people won't read the text. It's a sad truth, because the text is often essential to filling out the context, but most of the time people are busy or distracted or whatever else and are only going to look at the visuals.

As such, it is essential that the visualizations you create can stand on their own, supplying their own context and presenting their own conclusions. A person should be able to look at your graph and understand everything they need to interpret it.
Elements of a good visual

Let's try a second visualization.

Base Image

This is a much better visual. We have labels on the axes and a title. You can look at this and quickly understand that sales have been steadily rising for the past year and a half, dating back to January 2016. Because this is a single series of data, a legend isn't really necessary, but if you had multiple lines on a single graph a legend would be valuable.

It can be tedious to add these elements to the chart, get the colors right, and place everything in the right place and at the right size so it's all easily visible and comprehensible. That's ok, it really is worth it and it's a critical part of your job. You want your audience to be able to easily consume the information you're sharing, and this is a powerful way to ensure that.
Visuals imply a stance

Now, this lesson is all about narrative analytics, but we've been talking about visualizations in a relatively absolute way. They should always be easy to read. They should always have proper labeling.

But do they imply a narrative in the same way as we discussed earlier?

Of course! There are several different ways to present the same data, and each one invites slightly different conclusions. First, let's use the simple example of axes. Here's the same data as above, presented with different axes:

Base Image

While there is still an upward trend, it doesn't appear as stark as it did previously. This is because we've now rooted our y-axis at $0, rather than letting it float to $12,000. Neither of these plots is "right" or "wrong", but they do imply two different stories at first glance.

Of course there's also different plots that we could use, and each one tells a different story with the data.

Base Image

Before you move on, look at these different plots and think about how they convey very different information even though they come from the same data. As you move through the course, remember to make your visualizations as clear and precise as possible. They should have everything you need to understand them, and nothing you don't.

# Narrative Analytics Guided Example

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline

artists = pd.read_csv('assets/artist_data.csv')
works = pd.read_csv('assets/artwork_data.csv')

Narrative Analytics Guided Example

Here we're going to dive into a dataset and perform some analytics, working with a dataset from the [Tate](http://www.tate.org.uk/) 
in the UK. Also note that data and guided example makes a decent example for your capstone report.
Tate Collection Data Exploration
Data

We will be working with the Tate's dataset of artists and artworks. This data was released by the Tate, a collection of art museums in the UK, representing 70,000 works either owned by the Tate or jointly with The National Galleries of Scotland as part of their Artist Rooms Series.

For our purposes we are going to assume that it is representative of their larger collection and that it is also therefore representative of the Tate's art collecting in general post 1800 (the earliest acquisition in this dataset was acquired in 1823).

The dataset itself consists of 2 tables, artists and artworks. There are also individual json files for each artist and artwork, but we are not going to pull all of those individual files together.

The artists file contains an id, name, gender, year of birth, year of death, place of birth, place of death, and a url for the Tate's page on the artist. The works file contains accession number, id, artist, artist's role, artist id, title, date, medium, credit line, year, acquisition year, dimensions, inscription, and links to the image and the artwork's Tate webpage.

There are several challenges to this dataset. First, different kinds of artwork will demand different things from their fields. The role field also potentially holds a lot of interesting relationships to art practice.
Analytic Questions

#1 Who are the most popular artists in the Tate Collection? Are there any outliers in terms of amount collected?

Let's start with a simple question about popularity. Which artists and time periods has the Tate prioritized collecting? First we'll approach artists.

works.artist.value_counts().head(20).plot(kind='bar')

plt.ylabel('Artworks Count')

<matplotlib.text.Text at 0x107347c18>

This plot of artworks by artists for the top 20 artists really only shows us one thing (other than providing a list of the 20 most popular artists): The Tate has a lot of works by William Turner.

If anyone knows about this history of British museums this is not a surprise. Turner, an immensely popular artist in his day, left all of his works in his possession to Britain and therefore the Tate as part of what is called The Turner Bequest. It makes up a large portion of the Tate Britain's museum in London.

To look at the relative popularity of other artists let's remove Turner.

works.artist.value_counts().head(50)[1:51].plot(kind='bar', figsize=(10,5))

plt.ylabel('Artworks Count')

<matplotlib.text.Text at 0x10278fef0>

So there seem to be a few other exceptionally popular artists, with the first four or arguably six being collected in meaningfully larger numbers. Note Andy Warhol's presence here as one of the more currently well known artists on this list.

Remember, this is popularity in terms of pieces collected. We have no data about visits or webviews.

#2 Who are the artists in the Tate collection? How does that vary by geography, age, and living or dead?

len(artists)

3532

So there are 3,532 artists in the Tate collection. Where are they from? When looking into the placeOfBirth variable, there is a challenge, however. The format is inconsistent. Sometimes the birthplace includes a city, others just a country.

# Process data to create counts by country

​

# Split the place of birth on commas

locations = artists.placeOfBirth.str.split(',', 1).tolist()

locations = [x for x in locations if str(x) != 'nan']

countries = []

​

# Process countries and clean up text

for entry in locations:

    c = entry[-1]

    c = c.strip()

    countries.append(c)

countries = pd.DataFrame(countries, columns=['country'])

​

# Create numeric counts

cntry_counts = pd.DataFrame(countries.country.value_counts())

other = int(cntry_counts[10:].sum())

cntry_counts = cntry_counts[:10]

cntry_counts.loc[11] = other

cntry_counts = cntry_counts.rename(index={11: 'Other'})

​

# Generate Pie Chart

plt.figure(figsize=(10, 5))

plt.pie(cntry_counts.country)

plt.axis('equal')

plt.title('Artists Country of Birth')

plt.legend(cntry_counts.index)

<matplotlib.legend.Legend at 0x1074c5a20>

So, about half of the artists in the collection are from the UK, which again is not hugely surprising as this is a British collection. The two things of note we see here are that the US and Canada are the only two non-European countries in the top 10. Also, the other countries selection is quite large, with a very large number of countries having some representation in the tate collection and making up almost a quarter of their collection.

plt.plot(artists.yearOfBirth.value_counts().sort_index())

plt.title('Artists Born by Year')

<matplotlib.text.Text at 0x107eb2c88>

You can see that the closer to modern times we get, the more artists we have represented. You see some interesting peaks around the centuries that are perhaps worthy of further investigation. Maybe they're using something other than artist's names to talk about movements?

How does this compare to when artworks were acquired?

acquisition_df = pd.DataFrame(works.acquisitionYear.value_counts())

acquisition_df = acquisition_df.sort_index()

plt.plot(acquisition_df)

plt.ylabel('Works Acquired')

<matplotlib.text.Text at 0x107eeb208>

This shows a collection that seems to have several peaks in its growth. That is consistent with how museum collections tend to grow. While there is some steady acquisition, which is somewhat visible in the more modern years (though this is not a great visual of that), museums tend to see the majority of their growth from large gifts or bequests. The Turner Bequest, again, is the most visible. What does it look like without Turner?

acquisition_df = pd.DataFrame(works[works.artist != 'Turner, Joseph Mallord William'].acquisitionYear.value_counts())

acquisition_df = acquisition_df.sort_index()

plt.plot(acquisition_df)

plt.ylabel('Works Acquired')

<matplotlib.text.Text at 0x107eddeb8>

This shows a few more clear spikes but also a clear narrative that the collection has been growing more rapidly in recent years. This aligns with the skew towards contemporary artists.

Let's move on to one last subject: determining the portion of the artists who are living. For this, we'll use year of death as an indicator.

living = pd.DataFrame(artists.yearOfDeath.isnull())

living = pd.DataFrame(living.yearOfDeath.value_counts())

living.plot(kind='bar', legend=False)

plt.title('Artists Who are No Longer Living')

<matplotlib.text.Text at 0x1090af4e0>

This shows a surprisingly large portion of the artists collected by the Tate are still living. However, when put into context that the Tate is one of the largest supporters of contemporary art in Britain, hosting the largest prize for contemporary art with the Turner Prize, it does fit their profile.

#3 What are the most popular mediums and how does medium affect size?

So it would be tempting to start with medium just as the data provides it. However, this reveals a bit of a problem.

works.medium.value_counts().head(10)

Graphite on paper                            26167
Oil paint on canvas                           3383
Screenprint on paper                          2984
Lithograph on paper                           2721
Watercolour on paper                          1890
Etching on paper                              1793
Graphite and watercolour on paper             1680
Ink on paper                                   880
Intaglio print on paper                        820
Photograph, gelatin silver print on paper      750
Name: medium, dtype: int64

There are way too many kinds of medium, and with a level of subtlety that we don't really want. We'll group some together.

We're also dropping Turner here because he has 25,000 works on paper that skew all counts towards that.

# Remove Turner

turnerless_artworks = works[works['artist'] != 'Turner, Joseph Mallord William']

# Coerce to Numeric

turnerless_artworks.height = pd.to_numeric(turnerless_artworks.height, errors = 'coerce')

turnerless_artworks.width = pd.to_numeric(turnerless_artworks.width, errors = 'coerce')

turnerless_artworks.depth = pd.to_numeric(turnerless_artworks.depth, errors = 'coerce')

turnerless_artworks = turnerless_artworks[turnerless_artworks['units']=='mm']

turnerless_artworks = turnerless_artworks[turnerless_artworks.height.notnull()]

​

## The error is just because of how we did the conditional select and we don't need to be worried about it...

/Library/Frameworks/Python.framework/Versions/3.5/lib/python3.5/site-packages/pandas/core/generic.py:2773: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
  self[name] = value

# Aggregate to new medium_agg column

turnerless_artworks['medium_agg'] = 'other'

turnerless_artworks.loc[turnerless_artworks['medium'].str.contains("paper", na=False),'medium_agg'] = 'paper'

turnerless_artworks.loc[turnerless_artworks['medium'].str.contains("canvas", na=False),'medium_agg'] = 'canvas'

turnerless_artworks.loc[turnerless_artworks['medium'].str.contains("wood", na=False),'medium_agg'] = 'wood'

turnerless_artworks.loc[turnerless_artworks['medium'].str.contains("paint on", na=False),'medium_agg'] = 'other painted panel'

turnerless_artworks.loc[turnerless_artworks['medium'].str.contains("Bronze", na=False),'medium_agg'] = 'sculpture'

turnerless_artworks.loc[turnerless_artworks['medium'].str.contains("Plaster", na=False),'medium_agg'] = 'sculpture'

turnerless_artworks.loc[turnerless_artworks['medium'].str.contains("Marble", na=False),'medium_agg'] = 'sculpture'

turnerless_artworks.loc[turnerless_artworks['medium'].str.contains("Stone", na=False),'medium_agg'] = 'sculpture'

turnerless_artworks.loc[turnerless_artworks['medium'].str.contains("plate", na=False),'medium_agg'] = 'plate'

turnerless_artworks.loc[turnerless_artworks['medium'].str.contains("photograph", na=False),'medium_agg'] = 'photo'

​

turnerless_artworks['surface'] = turnerless_artworks.height * turnerless_artworks.width

turnerless_artworks[['medium_agg','height','width','depth','surface']].groupby('medium_agg').describe()

		depth 	height 	surface 	width
medium_agg 					
canvas 	count 	83.000000 	260.000000 	2.590000e+02 	259.000000
mean 	134.957831 	1776.396154 	3.424765e+06 	1495.119691
std 	355.563519 	1543.269130 	3.831638e+06 	890.336830
min 	5.500000 	105.000000 	1.260000e+04 	120.000000
25% 	27.500000 	729.250000 	5.518635e+05 	727.500000
50% 	35.000000 	1512.500000 	2.283380e+06 	1410.000000
75% 	53.000000 	2290.750000 	4.707936e+06 	2135.000000
max 	2185.000000 	16000.000000 	2.173195e+07 	4860.000000
other 	count 	953.000000 	1301.000000 	1.298000e+03 	1298.000000
mean 	761.288772 	1189.179554 	1.880836e+06 	960.942604
std 	1448.336740 	1866.683697 	4.996881e+06 	1019.110727
min 	3.000000 	6.000000 	1.681000e+03 	5.000000
25% 	125.000000 	273.000000 	8.754350e+04 	290.000000
50% 	300.000000 	620.000000 	3.955995e+05 	603.000000
75% 	750.000000 	1460.000000 	1.597850e+06 	1314.750000
max 	18290.000000 	37500.000000 	9.125394e+07 	10900.000000
other painted panel 	count 	442.000000 	4408.000000 	4.408000e+03 	4408.000000
mean 	76.997738 	1032.772913 	1.392090e+06 	960.962568
std 	290.694723 	820.503273 	2.247036e+06 	639.367519
min 	2.000000 	45.000000 	3.306000e+03 	50.000000
25% 	20.000000 	514.000000 	2.917325e+05 	508.000000
50% 	30.000000 	787.000000 	6.247550e+05 	762.000000
75% 	55.000000 	1270.000000 	1.558060e+06 	1244.250000
max 	5486.000000 	11900.000000 	3.623310e+07 	4580.000000
paper 	count 	160.000000 	19800.000000 	1.978000e+04 	19780.000000
mean 	277.478125 	417.212288 	2.608455e+05 	407.575925
std 	695.113346 	379.088368 	7.540381e+05 	326.287752
min 	1.000000 	15.000000 	2.370000e+02 	3.000000
25% 	28.250000 	200.000000 	3.904200e+04 	190.000000
50% 	45.000000 	320.000000 	1.029940e+05 	320.000000
... 	... 	... 	... 	... 	...
photo 	std 	467.421236 	2106.887208 	6.188098e+06 	962.547810
min 	18.000000 	90.000000 	1.332000e+04 	100.000000
25% 	25.000000 	303.500000 	9.896750e+04 	380.000000
50% 	39.500000 	690.000000 	3.884175e+05 	608.000000
75% 	146.500000 	1395.250000 	1.696120e+06 	1202.750000
max 	2015.000000 	19890.000000 	5.431500e+07 	4892.000000
plate 	count 	8.000000 	344.000000 	3.440000e+02 	344.000000
mean 	1997.625000 	347.148256 	1.258063e+05 	264.523256
std 	4215.212448 	478.247577 	4.437804e+05 	210.308546
min 	25.000000 	76.000000 	7.752000e+03 	102.000000
25% 	75.000000 	305.000000 	6.984500e+04 	229.000000
50% 	585.500000 	305.000000 	6.984500e+04 	229.000000
75% 	1107.750000 	305.000000 	6.984500e+04 	229.000000
max 	12360.000000 	8850.000000 	6.549000e+06 	2235.000000
sculpture 	count 	620.000000 	639.000000 	6.390000e+02 	639.000000
mean 	406.875806 	619.608764 	6.975306e+05 	765.388106
std 	504.036311 	791.822922 	1.405889e+06 	657.149556
min 	8.000000 	18.000000 	1.296000e+03 	19.000000
25% 	152.000000 	222.000000 	7.777050e+04 	304.000000
50% 	270.000000 	406.000000 	2.032000e+05 	533.000000
75% 	445.000000 	714.500000 	6.622965e+05 	1029.000000
max 	5800.000000 	11250.000000 	1.796402e+07 	3750.000000
wood 	count 	208.000000 	349.000000 	3.490000e+02 	349.000000
mean 	548.336538 	1067.189112 	2.160677e+06 	1065.908309
std 	923.748764 	1597.806055 	8.422669e+06 	1145.166249
min 	6.000000 	30.000000 	6.300000e+03 	35.000000
25% 	91.500000 	340.000000 	1.416000e+05 	400.000000
50% 	260.000000 	611.000000 	4.966000e+05 	756.000000
75% 	510.000000 	1073.000000 	1.247400e+06 	1310.000000
max 	6300.000000 	14850.000000 	1.324620e+08 	11960.000000

64 rows × 4 columns

​

turnerless_artworks[['medium_agg', 'height']].boxplot(by='medium_agg', figsize=(10,20))

​

<matplotlib.axes._subplots.AxesSubplot at 0x109093e48>

Now, that plot is so ghastly large that it's likely impossible to see all of it on a monitor at once. However, keeping it makes a point. There are some exceptional outliers here. The most striking is a steel piece by Miroslaw Balka measuring 37.5 meters high! We only included one of the plots, but it would be trivial to generate the same boxplot for width, depth, and surface area. Admittedly there are also some works on paper over 10 meters high.

However, the bottom part of the plot has more generally applicable conclusions to show. Plates are almost all the same size (this is things like copper plates by the way, not ceramic). Canvas is the largest in medium and 75th percentile, and therefore also the highest whisker.

So as one would expect different mediums are generally different sizes but there is huge variation in the collection, so trying to predict medium off of size could be very difficult.

Also just for fun, they have 27 works in the medium of "ink on banknote", so that's something. It's a series by Cildo Meireles.
