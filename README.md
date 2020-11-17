# python-baltimore-baskingridge-income-same-tract
## Background Information
Here, I recreated a [previous project](https://github.com/viv-sun/baltimore-baskingridge-income-and-same-tract), but used Python and Google Colaboratory to do the data analysis instead of Microsoft Excel. 

I compared data from Baltimore City, MD to Basking Ridge, NJ. All data is from [Opportunity Atlas](https://www.opportunityatlas.org/), which uses anonymous data that follows 20 million Americans from their childhood to their mid-30s in 2015. I focused specifically on __Household Income__ and __Percentage of Adults who Stayed in the Same Tract (SST)__. Household income refers to the average household income that a person (who grew up in this area in the past) has in 2014-15. The SST metric refers to the percentage of people who still live in the same Census tract that they grew up in. 

I was curious about the SST metric because I hadn't seen it as often as I had seen metrics like incarceration rate, high school graduation rate, etc. I wondered how it was related, if at all, to the household income that people would later have as adults. 

### Business Question 
How does one's annual household income affect if they, as adults, remain in the same Census tract in which they grew up? 

## Data Sources
[Google Colaboratory](https://colab.research.google.com/drive/1JwyPECzXniWTbxy00Tyl-9DqhfIUZhUr?usp=sharing) shows the code that I used for this data analysis.

[Baltimore Income Data]( link here ) shows the raw data for the Household Income metric in the general Baltimore, MD area.

[Baltimore Same Tract Data]( link here ) shows the raw data for the SST metric in the general Baltimore, MD area. 

[Basking Ridge Income Data]( link here ) shows the raw data for the Household Income metric in the 07920 Bernards Township area. 

[Basking Ridge Same Tract Data]( link here) shows the raw data for the SST metric in the 07920 Bernards Township area. 

## Data Analysis/Metrics 
I compared the Household Income metric against the SST metric for Baltimore, and again for Basking Ridge. 

### Graph for Baltimore Comparisons 
![alt text]( link to graph here ) 

I sorted the household income from low to high to make it easier to see the relationship (if any) between the two metrics. For the most part, it seems that there is not a clear relationship between household income and the percentage of adults who stayed in the same Census tract. However, towards the right side of the graph, household income shoots up and the percentage of adults who stayed in the same tract falls - it looks as if there is an inverse relationship for the two. 

### Graph for Basking Ridge Comparisons 
![alt text]( link to graph here )

We do need to keep in mind that this sample size is very limited and the range on both Y axes is small. However, it does show (what appears to be) an inverse relationship between the two metrics.  

## Summary 
The results of my data analysis this time (using Python) were very similar to my results from when I used Excel. 

Overall, the graphs (especially that of Baltimore) seem inconclusive. Both graphs appear to show a weak inverse relationship between household income and the SST metric (with Baltimore's graph showing a weaker overall relationship than that of Basking Ridge), but the lack of a clear/strong relationship is an answer in and of itself. It indicates that there are likely a plethora of other factors (in addition to household income) that may also play a part in determining if someone were to stay or leave the Census tract in which they grew up. 

These additional factors include: if people married and left the tract they grew up in; if they pursued higher education, and especially if their universities were within a commuting distance; if there is a brain drain from the area; if people have the income/resources to afford to stay in their childhood Census tracts, assuming if housing prices went up; or if people have the income/resources to leave their childhood Census tracts, assuming they want to leave. By no means is this an exhaustive list of reasons.

Moving forward, I am interested in looking at a larger sample size of data for the Basking Ridge/surrounding area to see if there would be a repeat of the weak relationship that appeared in the Baltimore graph. The Basking Ridge data was rather limited, with a sample size of only three data points. I would also be interested in looking at how the SST metric relates to other metrics available from Opportunity Atlas (like high school graduation rate, employment rate, etc.).

Perhaps the additional data may help identify some reasons why people may choose to stay vs leave, but we must also remember that metrics do not provide any insight into intentions. The decision to stay vs leave a tract is a nuanced and deeply personal one; it may not be properly reflected in just one or two metrics. Data, no matter how much we have and although it can provide us with significant insight into someone's decision-making process, does not fully account for the personal and/oor qualitative factors that can also affect a decision to stay vs leave.

### Python vs Excel
For this version of the project, I believe that the data analysis results were rather similar because I used the same raw data and the same steps for filtering and analyzing data (albeit with a different software). 

When working with Python, the thing that struck me the most was how quick and easy it was to work with the data. I didn't have to wade through and delete undesired columns or fiddle with Excel graphs (especially when trying to configure which axis should represent which column of data). It was a lot easier and a lot faster in terms of setting up the data analysis, especially for merging datasets together. 

I would still recommend using Microsoft Excel for filtering data, especially for a smaller dataset, simply because it is easier to visualize the dataset when  first starting out. However, I believe that Python would still be the mode of choice for me when it comes to merging datasets together and creating data visualizations. It was much easier and more straightforward to use Python to assign a certain column to each axis, as opposed to working with Excel and trying to "switch variables" when editing the data, and running into potential errors there.  




Highlight how using Python was different than using Excel and how you may or may not use both together in the future.
