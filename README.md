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

When we looked at our Fare data and Driver Data, in the form of a box-and-whisker plot,  we did not see any outliers.  Thus, we knew these data sets were not skewed from an outlier. 

<img width="404" alt="Screen Shot 2022-05-14 at 6 25 52 PM" src="https://user-images.githubusercontent.com/6634774/168449997-922f70db-9f65-467a-a350-b7ccaf605600.png"><img width="406" alt="Screen Shot 2022-05-14 at 6 28 23 PM" src="https://user-images.githubusercontent.com/6634774/168450040-be6e3b5a-7e0c-4488-bcf5-e67cb0735694.png">

## Pie Charts

Our next piece of analysis looked at the percentage of total fares, total drivers, and total rides by city type. It seemed clear to us, after reviewing these charts that the urban city-type was the ruler of this market by far.  Which, common-sensically, also made sense to our analysis team. 

<img width="339" alt="Screen Shot 2022-05-14 at 6 31 11 PM" src="https://user-images.githubusercontent.com/6634774/168450083-cbc96c9b-23a2-4888-a994-8b3940e911e3.png">

<img width="428" alt="Screen Shot 2022-05-14 at 6 31 28 PM" src="https://user-images.githubusercontent.com/6634774/168450086-eb1dfb76-d6e6-4241-a8b3-140152f3473c.png">

<img width="378" alt="Screen Shot 2022-05-14 at 6 31 42 PM" src="https://user-images.githubusercontent.com/6634774/168450092-4432333e-9b46-473d-8e6d-de4c5b984bd3.png">

## Aggregate Data

Next, we wanted a clean chart that showed each city type with the total rides, drivers, fares and the average fare per ride and driver.  This view would give us a clear picture as to how each city type was performing and with the data grouped, we could clearly see which city type was the most profitable. 

<img width="554" alt="Screen Shot 2022-05-14 at 6 33 25 PM" src="https://user-images.githubusercontent.com/6634774/168450122-a80b53a4-cacb-4a6e-b055-0f1f9ff7da50.png">

Based on this data, we can clearly see that Urban cities are the most profitable for pyBer while Rural would be the most profitable for a Driver; however, a driver will get far less rides in a rural setting when compared with suburban or urban.  The total number of rides is 10:1 Urban:rural and 5:1 Suburban:rural, it seemed clear to our team that a driver would have a greater chance to be profitable in an urban setting rather than a rural setting, this also held true for pyBer as a whole, as the total fares from an urban setting was 9:1 compared with rural, and 2:1 when compared with suburban. 

## 1st Quarter 2019

Our client wanted to look at the data from the first 1st quarter of 2019 (Jan - Apr), and wanted to see this data broken out on a line chart to indicate the change over time during this quarter. 

<img width="783" alt="Screen Shot 2022-05-14 at 6 38 31 PM" src="https://user-images.githubusercontent.com/6634774/168450234-6f9f66e5-e67a-4783-9cc6-92f4a72dd829.png">

Upon reviewing our chart, we determined that (once again), the urban ride-share setting was the most lucrative.  Additionally, we determined that there were peaks in rides during the end of february and begging of march in the urban cities. Infact, all 3 settings showed a peak in rides during the last week of Feb. With the urban cities showing a fairly steady revenue through mid-march.

## Suggestions moving forward
1. Based on this data, if pyBer is looking to get increase it's reach/profile, our team would highly suggest to focus on urban areas.  It is clear that the profitability is at minimum 2x greater than the next city type (suburban).
2. Resource allocation: It seems clear that allocating drivers towards big cities would be the most profitable; however, it may be lucrative for drivers to have bonuses/incentives to take rides in suburbs/rural areas as these are the areas that are the most profitable for a driver on a per-ride basis. 
3. Resource allocation part 2: Increasing the number of drivers from the end of february in all settings makes sense, then towards the beginning of march, shifting those resources towards the urban settings to offset the decrease in ride requests for suburbs/rural areas. This shift can mostly likely remain without consquence through the end of april.

## Further Analysis Needed
1. Analyzing the trends on the full year of 2019, will give us a better view of where/when to shift drivers from urban/suburban/rural areas. 
2. Analyzing the average ride costs on a yearly basis, would allow us to provide drivers with a better view of how they could increase their profits throughout the year. 
3. Analyzing the total drivers in an area during a given time period vs. how many rides are requested, would provide us with greater insights on where to suggest driver placement. 



