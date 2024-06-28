# Google-Data-Analytics-Capstone-Cyclistic-Case-Study
Course: [Google Data Analytics Capstone: Complete a Case Study](https://www.coursera.org/learn/google-data-analytics-capstone?specialization=google-data-analytics)

For this case study I will perform the tasks of a junior data analyst working on the marketing team at Cyclistic, a fictional company. 

## Quick links:
Data Source: [Divvy_Trips_2019](https://divvy-tripdata.s3.amazonaws.com/index.html) (Q1-Q4)

SQL Queries: 

[Data Combining](https://github.com/jp1999-oss/Google-Data-Analytics-Capstone-Cyclistic-s-Case-Study/blob/main/01.%20Data%20Combining)
[Data Exploration](https://github.com/jp1999-oss/Google-Data-Analytics-Capstone-Cyclistic-s-Case-Study/blob/main/02.%20Data%20Exploration)
[Data Cleaning](https://github.com/jp1999-oss/Google-Data-Analytics-Capstone-Cyclistic-s-Case-Study/blob/main/03.%20Data%20Cleaning)
[Data Analysis](https://github.com/jp1999-oss/Google-Data-Analytics-Capstone-Cyclistic-s-Case-Study/blob/main/04.%20Data%20Analysis)

Data Visualization: [Tableau](https://public.tableau.com/app/profile/justin.pena/viz/CyclisticsCaseStudy_17194634778200/Avg_BikeRideTimeBreakdown#1)

## Background
### Cyclistic
A bike-share program that features more than 5,800 bicycles and 600 docking stations. The program offers flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships.
Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members. Cyclistic’s finance analysts have concluded that annual members are much more profitable
than casual riders.

## Scenario
The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these
insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations.

## Ask
### Anlaysis Question
1. How do annual members and casual riders use Cyclystic bikes differently?

## Prepare
### Data Source: 
1. [Divvy_Trips_2019_Q1](https://divvy-tripdata.s3.amazonaws.com/index.html)
2. [Divvy_Trips_2019_Q2](https://divvy-tripdata.s3.amazonaws.com/index.html)
3. [Divvy_Trips_2019_Q3](https://divvy-tripdata.s3.amazonaws.com/index.html)
4. [Divvy_Trips_2019_Q4](https://divvy-tripdata.s3.amazonaws.com/index.html)

Note: The datasets have a different name because Cyclisticis a fictional company. For the purposes of this case study, the datasets are appropriate andwill enable you to answer the business questions. The data has been made available by Motivate International Inc. under this ([license](https://divvybikes.com/data-license-agreement).)

## Data Organization
There are 4 files containing information about every registered bike ride with a Cyclistic bike in 2019. The tables columns names are: trip_id,start_time,end_time,bikeid,tripduration,from_station_id,from_station_name,to_station_id,to_station_name,usertype,gender,birthyear,day_of_week,month,total_ride_time_mins. The columns day_of_week, month, and total_ride_time_mins were added during cleaning.

## Process
PostgreSQl server used to store the databases, and pg Admin used to interact and manage the databases.

## Combining the Data
SQL Query: [Data Combining](https://github.com/jp1999-oss/Google-Data-Analytics-Capstone-Cyclistic-s-Case-Study/blob/main/01.%20Data%20Combining)

Explanation: The Divvy_Trips_2019 data was split up into 4 csv files. One file for each quarter of the year. Through this query I am able to combine all 4 tables into 1 new table, Divvy_Trips_2019_Combined_Data with a total of 3,818,004 rows.

## Data Exploration
SQL Query: [Data Exploration](https://github.com/jp1999-oss/Google-Data-Analytics-Capstone-Cyclistic-s-Case-Study/blob/main/02.%20Data%20Exploration)

Explanation: During data exploration I familiarised myself with some key factors of the data set, such as, the number of rows,rows containing NULL values, rows with outlier data that can skew our analysis, and potential data duplicates.

## Data Cleaning
SQL Query: [Data Cleaning](https://github.com/jp1999-oss/Google-Data-Analytics-Capstone-Cyclistic-s-Case-Study/blob/main/03.%20Data%20Cleaning)

Explanation: During the data cleaning phase, I removed all outlier data that could skew our analysis. I also removed all rows containg NULL values to ensure we could extract and analyze all aspects of every ride. The day_of_week, month, and total_ride_time_mins columns were added. The data is cleaned and ready for analysis.

## Data Analysis
SQL Query: [Data Analysis](https://github.com/jp1999-oss/Google-Data-Analytics-Capstone-Cyclistic-s-Case-Study/blob/main/04.%20Data%20Analysis)

Data Visualization: [Tableau](https://public.tableau.com/app/profile/justin.pena/viz/CyclisticsCaseStudy_17194634778200/Avg_BikeRideTimeBreakdown#1)

Explanation: During the data analysis phase, I ran queries to explore the difference in bike usage between annual members and casual riders on the monthly, daily, and hourly timeline. I then utilized Tableau, a visualization program to create line graphs to display the findings. 

## Share

<img width="844" alt="Screen Shot 2024-06-27 at 3 06 32 PM" src="https://github.com/jp1999-oss/Google-Data-Analytics-Capstone-Cyclistic-s-Case-Study/assets/173986410/d24e855d-8cbd-421e-b08d-c9018d21587b">

Explanation: The Cyclysitc subscribers take more trips than the Cyclsitic members throughout the month, day, and hour, which is expected. In the peak months May thru October, the subscribers ride just under 5 times more than the members. In the peak days Mon-Friday, subscribers ride almost 10 times more than the members. During the peak hours 7AM-8AM, the subscribers ride around 30 times more than the members, and during the other peak hours 4PM-6PM, the subscribers ride around 10 times more than the members. We can assume these trends are due to the Cyclystic subscribers using the bikes to commute to and from work during the week, and the members use the bikes for leisure throughout the afternoon and night on the weekends mostly. Both groups peak during the warmer months, and their total rides decrease during the colder months.

<img width="998" alt="Screen Shot 2024-06-27 at 3 12 19 PM" src="https://github.com/jp1999-oss/Google-Data-Analytics-Capstone-Cyclistic-s-Case-Study/assets/173986410/df641759-1a37-4b9f-91c4-3813eb358a83">

Explanantion: The Cyclystic members on average, enjoy longer bike rides throughout the month, day, and hour. This is interesting because while their total bike ride is significantly less than subscribers, the members' total ride time in the peak months May thru Oct. is almost 3 times longer than subscribers. The results are similar for the total ride time for bike rides throughout the day and hour.

Summary:
Riding Patterns: Cyclistic subscribers mostly ride on a daily schedule at certain hours, presumably because they are commuting to and from work. Cyclystic members ride dispersion is more spread out and spontaneous, presumably because they use the bike for leisure. Both subscribers and members take more rides during the spring and summer.

Riding Frequency and Duration: Cyclystic subscribers ride more frequently for less amount of time, presumably because they are commuting to and from work. Cyclystic members ride more infrequent, however when they do ride it is almost 3 times longer than subscribers rides.

## Act

1. Develop a reward system for Cyclystic subcribers. The reward system will offer local promotions or treats for accumulated ride time and consistency. With this system, current Cyclistic subscribers will be rewarded because of their consistency, and Cyclystic members will convert to subscribers to enjoy the benefits of their longer ride times. A reward could be a free smoothie from a local juicery, this engages the local community, expands Cyclystic's reach and creates motivated users.

2. Offer a flexible 6 month subscriber package, and for first time subscribers they will get the remainder of the first year free. This model supports the peak months, May thru October and allows the newly subscribed rider to experience the subscriber package for the entire year at a discount. This recommendation relies on the subscriber to find unrealized value in the six months of free riding, and if the value is found they will continue to renew as an annual subscriber.

3. Launch a marketing campaign throughout the locations most frequented by Cyclystic members. The campaign will focus on the value of an annual subscription rather an every time use charge, and this can convert members to subscribers.




