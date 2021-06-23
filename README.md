# Oahu Weather Analysis
## Overview
The purpose of this project is to produce and analyse weather statistics for the island of Oahu, Hawaii for the months of June and December. The raw weather data were given in a SQLITE file containing information on a number of weather stations and a list of dated weather reports from Jan. 1, 2010 - Aug. 23, 2017. The weather data were then extracted from this file using Python's SQLAlchemy library. The data were imported into Pandas Data Frames and analysed using Pandas' ```DataFrame.describe()``` method.

## Results
The summary statistics gathered for the two months are as follows (tobs = temperature observations, all temperature data in degrees F):

### June

![JuneSummary](https://user-images.githubusercontent.com/80861610/123155532-38ba7b80-d436-11eb-9e09-7a8d7569e368.png) 

### December

![DecemberSummary](https://user-images.githubusercontent.com/80861610/123155814-8e8f2380-d436-11eb-85dd-9ff9ea9a5381.png)

Some key differences between the weather statistics for these months are:
* The mean temperatuer for June (~74.9) was about 4 degrees higher than for December (~71.0). 
* The minimum temperature for for June (64) was 8 degrees higher than for December (56).
* The median temperature for June (75) was 4 degrees higher than for December (71)

## Summary 
What the statistical analysis shows is unsurprising: Hawaii has similar temperatures in both June and December, but December is slightly cooler.

The analysis is in need of significant improvement given that the provided data does contain the same number of reports for each date. This is clear from a brief examination of the reports sorted by date. This is also likely the reason that in the data for both June and December, different stations contributed vastly different numbers of reports. The result, in any case, is that differnt days are not equally represented in the summary statistics, i.e., there are more measurements for some dates than others. 

Two additional queries that could be done to correct this would be: (1) do the same analysis with the restraint that results from only one station are included in the output, (2) create a new data frame where the rows are the averages of all observations on a given date, and do the same analysis on that data frame. Either of these would ensure that only one observation is being associated with each date.
