# PyBer_Analysis

# Overview

Our client at PyBer, asked us to look at their ride-share data from the year 2019.  Within the data, we were asked to look at how drivers, fares and rides were spread over city types (Urban, Suburban and Rural) and find trends amongst the analysis. 

# The point?

1. To suggest where/when PyBer couuld add/subtract drivers for a given type of city. 
2. To determine which type of city was the most profitable.
3. To determine the percentages of drivers, rides and fares by city type.

# Resources
1. Python
2. mathplotlib
3. city_data.csv
4. ride_data.csv
5. numpy
6. jupyter notebook

# Analysis 

The first step was the integrade the city and ride data into one dataframe, to do this we had to check if the data was clean, and if it as not, we needed to clean it.  We were in luck, because after we ran our initial check, we discovered our client provided us with clean data for us to work with.  

Next we merged that data based on the city, as both CSV files (and resulting data frames) each contined the name of the city, we were able to combine the data based on that column. 

To start our initial analysis we wanted to provide ourselves with some basic data:
1. Dataframes for each city type (urban, suburban and rural)
2. A total count of rides for each city type.
3. The average fare cost per city.

## Bubble/Scatter Plot

From this data we were able to create a scatter plot that showed the average fare, the number of rides per city with a cirlce size that indicated the driver count per city.  Each bubble indicated a single city within the data set. (analysis/Fig1.png)

<img width="507" alt="Screen Shot 2022-05-14 at 6 18 05 PM" src="https://user-images.githubusercontent.com/6634774/168449817-3c538626-be30-48e8-9aad-20637528b58f.png">

This bubble plot showed us that urban cities had the most rides, the most drivers and the lowest avarage fare per ride.  This data made sense as the more densly populated an area, we would assume that there would be more drivers, more rides and because the general trip time would most likely be shorter, the average fare would be lower.   This was substatiated in our initial bubble plot shown above.

## Outliers? 

We noted in the bubble plot there there may be some data that was well outside our means and standard deviations.  So we took our city type data ran it through our standard measures of central tendencies (mean/mode/median), and created a box and whisker plot that would show us if any outliers existed. We found that in our ride count data, we had at least one such outlier. 

<img width="407" alt="Screen Shot 2022-05-14 at 6 22 06 PM" src="https://user-images.githubusercontent.com/6634774/168449921-3045b6fd-a37d-4ce6-a6b1-a98d9e863a8f.png">

The urban city data was the only set that had an outlier, we determined this city was "West Angela" but we didn't feel as if this skewed our data. 

When we looked at our Fare data and Driver Data, in the form of a box-and-whisker plot,  we did not see any outliers.  

<img width="404" alt="Screen Shot 2022-05-14 at 6 25 52 PM" src="https://user-images.githubusercontent.com/6634774/168449997-922f70db-9f65-467a-a350-b7ccaf605600.png"><img width="406" alt="Screen Shot 2022-05-14 at 6 28 23 PM" src="https://user-images.githubusercontent.com/6634774/168450040-be6e3b5a-7e0c-4488-bcf5-e67cb0735694.png">





