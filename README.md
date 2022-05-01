# PyBer_Analysis
To Perform an Exploratory Analysis for Pyber,a python based ride sharing app company to improve the access to ride sharing services and determine affordability for underserved neighborhoods.

## Overview of Analysis
Pyber wants to perform analysis on ride sharing data among various types of cities like Urban,Suburban,Rural.To aid this process we create several types of visualizations,to tell compelling story about the data.In order to perform this analysis we have used Python's two dimensional ploting library known as Matplotlib.It produces quality figures of various data series to tell a visual story of data.Telling a visual story from data means to present complex findings in a way that's informative and engaging to all stakeholders.Data Visualization allow audience to absorb more information quickly as well as to detect design patterns,trends,correlations and outliers that are usually difficult to show in thousand of rows.It helps for project planning and decision making.
## Purpose of Analysis
The purpose of the project is to analyze the data,by calculating certain metrics like total weekly fares for each city type.Datasources like ride and city data are used for calculating some of the metrics like total rides,total drivers,total fares,average fare per ride and average fare per driver for each city type.A Multi line plot is plotted based upon the metrics calcualted.By seeing the results we can determine how the ride sharing app is used among various cities

## Softwares Used:
Sources:
Language:Python
Library:Pandas,Matplotlib


## Results
The Pyber Summary Dataframe is created based upon the data gathered by performing certain operations like groupby() and count() on the given datasets.
The total rides in the pyber summary dataframe indicates that there were more rides in urban cities with 1625 compared to suburban which has 625 and rural which has only 125 rides.The pyber's overall ride is contributed by urban cities.
When we see total drivers column we can see that there are highest number of drivers in urban city of 2405,where as suburban has 490 drivers and rural has only 78 drivers.By seeing the total fares column,we can tell urban cities has largest revenue because it has more number of rides compared to other city types.The average fare per ride column shows that the average fare in rural is $10 more than the urban cities.Where as the suburban is around $31 per ride.
So we can say that the riders of rural has to spend more.We can also see that average fare per driver is high in rural with $55.49,which shows that it is better for drivers in rural city.
<img src = "" width = 500>

In order to create multi line graph that shows the total fares for each week by city type.We need to use pivot function to categorize the data as rural,suburban and urban with date as index.The data is filtered with in January to April 2019 qnd then resampling is performed to calculate the total fares based on each week.

With  the calculated data we can plot multi line chart using object oriented interface method,In which fares aer on Y axis and weeks of each city type are on y axis.

The chart implies that urban cities total fares range between $1600 to $2500 with in 4 month period.Where as in rural city we can see that the fare was around $300 through out the period.The suburban is in the middle of the chart,which shows the fares are between $600 to $ 1200.

## Summary
By seeing the graph,we can say that there were peak in the fares in all the cities during the 4th week of February.
We can see that the ride sharing app is more demand in urban cities with more number of rides.
By increases the cost per ride a little in urban cities,we can increase in the revenue of the company.


## Summary
