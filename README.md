# PyBer_Analysis
To Perform an Exploratory Analysis for Pyber, a Python-based ride-sharing app company, improve access to ride-sharing services and determine affordability for underserved neighborhoods.

## Overview of Analysis
Pyber wants to analyze ride-sharing data among various types of cities like Urban, Suburban, and Rural. To aid this process, we create different visualizations to tell a compelling story about the data. To perform this analysis, we have used Python's two-dimensional plotting library known as Matplotlib. It produces quality figures of various data series to tell a visual data story. Telling a visual story from data means presenting complex findings that are informative and engaging to all stakeholders. Data Visualization allows the audience to absorb more information quickly and detect design patterns, trends, correlations, and outliers that are usually difficult to show in thousands of rows. It helps with project planning and decision-making.

## Purpose of Analysis
This project aims to analyze the data by calculating certain metrics like total weekly fares for each city type. Data sources like ride and city data are used for calculating some of the metrics like total rides, total drivers,total fares, average fare per ride, and average fare per driver for each city type. A Multiline plot is plotted based upon the metrics calculated.By seeing the results, we can determine how the ride-sharing app is used in various cities.

## Softwares Used
*DataSources*: [ride_data.csv](https://github.com/fathi129/PyBer_Analysis/blob/master/Resources/ride_data.csv), [city_data.csv](https://github.com/fathi129/PyBer_Analysis/blob/master/Resources/city_data.csv), 
[PyBer_ride_data.csv](https://github.com/fathi129/PyBer_Analysis/blob/master/Resources/PyBer_ride_data.csv).<br>
*Software used*: Jupyter Notebook 6.4.5.<br> 
*Libraries*: Panda,Matplotlib <br>
*Language*: Python 3.9.7. 

## Overview of the code
To open and read the CSV file, we need to import the corresponding dependencies. The file path is specified using the join() method so that based upon the operating system; the direct path is set.<br>
<img src = "https://github.com/fathi129/PyBer_Analysis/blob/master/Screenshots/csvpath.png" width = 600><br>
The CSV files are converted in to DataFrames, and they are merged using `merge()` method. The total rides are calculated based on the ride count and grouped by type of the cities. The same is done for calculating the total drivers,total fare.The average fare per driver and per ride are calculated based on the above calculations. Finally, the calculated result are displayed in the Pyber summary Dataframe.<br>
<img src = "https://github.com/fathi129/PyBer_Analysis/blob/master/Screenshots/calc.png" width = 800><br>
To create a multi-line plot that shows total weekly fares for each city type, we need to perform a sum operation on the fares, and they should be grouped by date and type. The index is reset by using the `reset_index()` method. The pivot table is created with index as date, columns as city types, and values as fares.<br>
<img src = "https://github.com/fathi129/PyBer_Analysis/blob/master/Screenshots/pivot.png" width = 800><br>
The new data frame is created from the pivot table by specifying month range criteria from January to April 2019. The date type of date index is converted to DateTime using the to_datetime() method.The resample() method is applied on the DataFrame to create the fares based on the each week for each city type.<br>
<img src = "https://github.com/fathi129/PyBer_Analysis/blob/master/Screenshots/Resample.png" width = 800><br>
The results are plotted using `plot()` method, and suitable titles are given for y axis,title of the chart, and the chart is saved using `savefig()` method. Final chart is displayed by using `show()` method.

## Results
The Pyber Summary Dataframe is created based upon the data gathered by performing specific operations on the given datasets. The total rides in the pyber summary data frame indicate significant demand for riders in urban cities with 1625 rides compared to suburban, which have 625 rides, and rural, which have only 125 rides. The pyber's overall ride is contributed by urban cities.<br>
<img src = "https://github.com/fathi129/PyBer_Analysis/blob/master/Screenshots/%20Pyber_summary_DataFrame.png" width = 900><br>

When we see total drivers column, we can see that there is the highest number of drivers in the urban city of 2405, where as suburban has 490 drivers and rural has only 78 drivers. By seeing the total fares column, we can tell that urban cities have the largest revenue because they have more rides than other city types. The average fare per ride column shows that the average fare in rural is $10 more than the urban cities. Where as the suburban is around $6 more than the urban cities. So we can say that the riders in rural have to spend more money for a ride. We can also see that the average fare per driver is high in rural with $55.49, which is 3 times more than the urban.
To create multi line graph that shows the total fares for each week by city type. We need to use the pivot function to categorize the data as rural, suburban and urban with the date as an index.<br>
<img src = "https://github.com/fathi129/PyBer_Analysis/blob/master/Screenshots/pivottable.png" width = 600><br>
The data is filtered from January to April 2019, and resampling is performed to calculate the total fares based on each week.<br>
<img src = "https://github.com/fathi129/PyBer_Analysis/blob/master/Screenshots/Resampled_DataFrame.png" width = 600><br>
With the calculated data, we can plot multi line chart using object-oriented interface method, In which fares are on the Y-axis and weeks of each city type are on the X-axis.<br>
<img src = "https://github.com/fathi129/PyBer_Analysis/blob/master/Screenshots/PyBer_fare_summary.png" width = 900><br>
The chart implies that urban cities total fares range is high between $1600 to $2500 within 4 month period. Whereas in rural city we can see that the fare was around $300 throughout the period. The suburban is in the middle of the chart, which shows the fares are between $600 to $1200.There is a decline during the start of the January and end of April for all the cities.
- By seeing the graph, we can say that there was a peak in the fares in all the cities during the 4th week of February.
- The urban city has the highest revenue during 2nd and 4th week of March.
- We can see that the ride sharing app is more demand in urban cities with more number of rides.
- By increasing the cost per ride a little in urban cities, we can grow the company's revenue.

## Summary
Based on the analysis performed, the business recommendations for Pyber to address the disparities among the city types are
- Urban cities have great demand for riders, and its total fare is high, contributing to most of the company's revenue. We can say that Urban cities are the best performing city compared to other city types, so more investment has to be made in Urban cities to have more profits.
- Rural cities have the least demand for rides, and their total fare is less, But we can see that the average fare per ride is high, which shows that if we improve more number of rides, the company's revenue would be improved.
- Increasing the number of drivers in rural and suburban would improve the wait time for the riders to use the service.
- The cost of rides in rural areas should be decreased to encourage more riders to use the service.
- Suburban cities are middle-performing cities compared to other cities.
- In rural cities, We need to calculate the wait time for the riders so that we can provide better service for them by increasing the number of drivers.


