# python-baltimore-baskingridge-income-same-tract
## Background Information
Here, I recreated a [previous project](https://github.com/viv-sun/baltimore-baskingridge-income-and-same-tract), but used Python and Google Colaboratory to do the data analysis instead of Microsoft Excel. 

I compared data from Baltimore City, MD to Basking Ridge, NJ. All data is from [Opportunity Atlas](https://www.opportunityatlas.org/), which uses anonymous data that follows 20 million Americans from their childhood to their mid-30s in 2015. I focused specifically on __Household Income__ and __Percentage of Adults who Stayed in the Same Tract (SST)__. Household income refers to the average household income that a person (who grew up in this area in the past) has in 2014-15. The SST metric refers to the percentage of people who still live in the same Census tract that they grew up in. 

I was curious about the SST metric because I hadn't seen it as often as I had seen metrics like incarceration rate, high school graduation rate, etc. I wondered how it was related, if at all, to the household income that people would later have as adults. 

### Business Question 
How does one's annual household income affect if they, as adults, remain in the same Census tract in which they grew up? 

## Data Sources
[Google Colaboratory](https://colab.research.google.com/drive/1JwyPECzXniWTbxy00Tyl-9DqhfIUZhUr?usp=sharing) shows the code that I wrote and used for this data analysis.

[Baltimore Income Data](https://github.com/viv-sun/python-baltimore-baskingridge-income-same-tract/blob/main/Baltimore_Income%20Data.csv) shows the raw data for the Household Income metric in the general Baltimore, MD area.

[Baltimore Same Tract Data](https://github.com/viv-sun/python-baltimore-baskingridge-income-same-tract/blob/main/Baltimore_Same%20Tract%20Data.csv) shows the raw data for the SST metric in the general Baltimore, MD area. 

[Basking Ridge Income Data](https://github.com/viv-sun/python-baltimore-baskingridge-income-same-tract/blob/main/Basking%20Ridge_Income%20Data.csv) shows the raw data for the Household Income metric in the 07920 Bernards Township area. 

[Basking Ridge Same Tract Data](https://github.com/viv-sun/python-baltimore-baskingridge-income-same-tract/blob/main/Basking%20Ridge_Same%20Tract%20Data.csv) shows the raw data for the SST metric in the 07920 Bernards Township area. 

## Data Analysis/Metrics 
I compared the Household Income metric against the SST metric for Baltimore, and again for Basking Ridge. 

### Graph for Baltimore Comparisons 
![alt text](https://github.com/viv-sun/python-baltimore-baskingridge-income-same-tract/blob/main/Baltimore-Household%20Income-Tract%20Graph.jpg) 

![alt text](https://github.com/viv-sun/python-baltimore-baskingridge-income-same-tract/blob/main/Baltimore-SST-Tract%20Graph.jpg)

I sorted the household income from low to high to make it easier to see the relationship (if any) between the two metrics. For the most part, it seems that there is not a clear relationship between household income and the percentage of adults who stayed in the same Census tract. However, towards the right side of the graph, household income shoots up and the percentage of adults who stayed in the same tract falls - it looks as if there may exist an inverse relationship for the two. 

This observation remains the same as the one I previously drew from my Excel analysis.

### Graph for Basking Ridge Comparisons 
![alt text](https://github.com/viv-sun/python-baltimore-baskingridge-income-same-tract/blob/main/Basking%20Ridge-Household%20Income-Tract%20graph.jpg)

![alt text](https://github.com/viv-sun/python-baltimore-baskingridge-income-same-tract/blob/main/Basking%20Ridge-SST-Tract%20graph.jpg)

We do need to keep in mind that this sample size is very limited and the range on both Y axes is small. However, it does show (what appears to be) an inverse relationship between the two metrics. 

This observation remains the same as the one I previously drew from my Excel analysis.

## Summary 
The results of my data analysis this time (using Python) were very similar to my results from when I used Excel. 

Overall, the graphs (especially that of Baltimore) seem inconclusive. Both graphs appear to show a weak inverse relationship between household income and the SST metric (with Baltimore's graph showing a weaker overall relationship than that of Basking Ridge), but the lack of a clear/strong relationship is an answer in and of itself. It indicates that there are likely a plethora of other factors (in addition to household income) that may also play a part in determining if someone were to stay or leave the Census tract in which they grew up. 

These additional factors include: if people married and left the tract they grew up in; if they pursued higher education, and especially if their universities were within a commuting distance; if there is a brain drain from the area; if people have the income/resources to afford to stay in their childhood Census tracts, assuming if housing prices went up; or if people have the income/resources to leave their childhood Census tracts, assuming they want to leave. By no means is this an exhaustive list of reasons.

Moving forward, I am interested in looking at a larger sample size of data for the Basking Ridge/surrounding area to see if there would be a repeat of the weak relationship that appeared in the Baltimore graph. The Basking Ridge data was rather limited, with a sample size of only three data points. I would also be interested in looking at how the SST metric relates to other metrics available from Opportunity Atlas (like high school graduation rate, employment rate, etc.). It would also be a good idea to look at other towns within Bernards Township (the township to which Basking Ridge belongs) to see if this weak relationship exists there, too. 

Perhaps the additional data may help identify some reasons why people may choose to stay vs leave, but we must also remember that metrics do not provide any insight into intentions. The decision to stay vs leave a tract is a nuanced and deeply personal one; it may not be properly reflected in just one or two metrics. Data, no matter how much we have and although it can provide us with significant insight into someone's decision-making process, does not fully account for the personal and/oor qualitative factors that can also affect a decision to stay vs leave.

### Python vs Excel
For this version of the project, I believe that the data analysis results were rather similar because I used the same raw data and the same steps for filtering and analyzing data (albeit with a different software). However, I did run into an issue in Python: Some neighborhoods in Baltimore City are large enough to encompass multiple tracts, which led to issues creating the line graph if the neighborhood name were used on the x-axis. This was an issue that I hadn't realized/come across, for whatever reason, during my original Excel analysis. In order to remedy this, I opted to use the tract numbers instead of neighborhood names for Baltimore City data visualizations. Tract numbers, while useful when working across large data sets, are harder for the general public to interpret than the use of neighborhood names. 

For the Basking Ridge data visualizations, I used tract numbers for both the Excel and Python data visualizations because Basking Ridge is large enough to encompass three tracts. However, this was not an issue in terms of interpretation because three tracts is not a huge sample size and all three tracts are from Basking Ridge. It becomes more difficult to interpret if there are a large number of neighborhoods involved (as in Baltimore City) and some, but not all, neighborhoods cover multiple tracts.

I found working with Python more difficult than working in Excel largely because 1) I am not as familiar with Python as a coding language and 2) it was more difficult to check the data in Python as I wrote new code (to see if my action yielded the desired results) than it was in Excel. I spent the bulk of my time trying to figure out small syntax errors/understand how the code worked and, at times, being (slightly) frustrated that my code wasn't working. 

However, one plus of Python was how easy it was to rename columns or delete undesired columns, as well as to create simple data visualizations from data sets with more than two columns. For data sets with a multitude of columns, it could become annoying to side-scroll and select which columns to delete and which to keep. In Python, all I had to do was write the name of the column to delete it - there was no need to hold down the ctrl button and no fear of accidentally selecting the wrong column. Additionally, Excel could be difficult to configure to create or edit graphs when it comes to assigning a variable to an axis; Python was more straightforward when it came to assigning a variable to an axis, especially for larger data sets. 

I would still recommend using Microsoft Excel for filtering data, especially for a smaller dataset, simply because it was easier to check my work as I go along. However, I believe that Python would be ideal for simple data visualizations. I will have to figure out how Python can be used for more complex data visualizations, like a combination line-and-bar graph (instead of having separate graphs for each); I imagine that it may prove easier to configure than Excel.
