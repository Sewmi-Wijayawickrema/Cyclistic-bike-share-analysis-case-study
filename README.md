# Cyclistic-bike-share-analysis-case-study
### Analysis of Cyclistic bike-share data to identify trends and improve customer conversion.
<p align="center">
<img width="519" alt="cover" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/img_sql/cover.webp">
</p>

#### Data Source: [divvy_tripdata](https://divvy-tripdata.s3.amazonaws.com/index.html)
## Introduction
This case study showcases a data analysis project done for the Google Data Analytics Professional Certificate course, Capstone Project, by concentrating on Cyclistic, a bike-share company in Chicago.

As a jonior data analyst in the marketing analyst team, the case objective is to develop a new marketing strategy to maximize the number of annual members. From the insights after going through the stages of business analysis process, the team will design a new marketing strategy to convert casual riders into annual members.

In order to answer the key buisness questions the analysts will follow the stages of data analysis process :-
<p>•	Ask </p>
<p>•	Prepare </p>
<p>•	Process  </p>
<p>•	Analyse</p>
<p>•	Share</p>
<p>•	Act  </p>


## Data Analysis Process
## Ask Phase:
##### Guiding question and answer
<p>• Key Question : How do annual members and casual riders use Cyclistic bikes differently? 
  </p>

In this phase, the analysis will be guided by the following questions to realize how annual members and casual riders use Cyclistic bikes differently. 
<p> </p>
<p>•	Percentage of Casual Riders vs Annual Members </p>
<p>•	Percentage of Rides per Month </p>
<p>•	Number of Rides per Day</p>
<p>•	Proportion of Rides by Bike Type </p>
<p>•	Percentage of rides per Season</p>
<p>•	Proportion of rides in Each Time Zone </p>
<p>•	Frequency of Rides per Hour</p>
<p>•	Average Ride Duration by Day</p>

## Prepare Phase:
The following analysis is made up of monthly files for January 2022 through December 2022 which consists the latest data of the past 12 months. 
After extracting all 12 files using *Excel, the table is consisted of thirteen columns pertaining to the bike trips.
And the coloumns issue data on the ride ID, rideable type, start and end station ID’s and locations, coordinates, and membership type for each sheet.

The data set consists of 13 variables, as shown in the following:
<p>1.ride_id (STRING): Unique ID assigned to each ride </p>
<p>2.	rideable_type (STRING):	classic, docked, or electric </p>
<p>3.started_at (TIMESTAMP):	Date and time at the start of trip </p>
<p>4. ended_at (TIMESTAMP): Date and time at the end of trip</p>
<p>5. start_station_name (STRING): Name of the station where the ride journey started from</p>
<p>6. start_station_id (STRING): ID of the station where the ride journey started from</p>
<p>7. end_station_name (STRING): Name of the station where the ride trip ended at</p>
<p>8. end_station_id	(STRING): ID of the station where the ride trip ended at </p>
<p>9. start_lat	(FLOAT): Latitude of starting station</p>
<p>10. start_lng (FLOAT):	Longitude of starting station</p>
<p>11. end_lat (FLOAT): Latitude of ending station</p>
<p>12. end_lng (FLOAT):	Longitude of ending station</p>
<p>13. member_casual (STRING): Type of membership of each rider</p>




## Process Phase:

#### <p>1.	Data Cleaning in Excel:</p> 
- The dataset was refined, inconsistencies were addressed, and the ride length information was formatted appropriately for subsequent analysis after cleaning data.

###### <p>2. Checking for Duplicates:</p>
- The duplicate values were searched and then removed using through the “Remove Duplicates” feature in Excel. This helped ensure data integrity and eliminate any duplicated entries if there are any.
###### <p>3. Validating Column Values:</p>
- The values in some specific columns, such as 'rideable_type' and 'member_casual', are verified to make sure the consistency and accuracy of the data set. Valid values such as 'classic_bike', 'docked_bike', 'electric_bike' for 'rideable_type', and 'casual_member' for 'member_casua', were retained to validate data.
###### <p>4. Removing Blank Values:</p>
- All columns were checked for incomplete or blank values. Rows with missing values (like start_station_name,end_station_name, start_station_id and end_station_id) were removed to clarify the completeness of data.
###### <p>5. Removing Unwanted Columns: </p>
- Columns start_lat,end_lat, start_lng and end_lng are not relevant to the given analysis. Therefore, those were removed from each file to focus only on the relevant variables.
###### <p>6. Adding the Ride Length Column:</p>
- A new column which is named as “ride_length” was added and it was used to calculate the duration of each ride. The values of the column were acquired by subtracting started_at timestamp from ended_at timestamp.
###### <p>7. Setting the Time Format:</p>
- The “Format > Cells > Time > 37:30:55” method was used to format the ride_length according to “HH:MM:SS”. It is to clarify that the ride duration was given in standardized format.
###### <p>8. Applying Conditional Formatting:</p>
- To highlight ride lengths that fell outside the desired range, conditional formatting was applied to the ride_length column. If a ride length is less than one minute or greater than 24 hours, they were formatted differently, to easily identify for further analysis.
###### <p>9. Sorting the Table:</p>
- To keep data consistency the table was sorted in ascending order based on the started_at column.

#### <p>•	Data Transformation in SQL: </p>

###### <p>1. Importing Data: </p>
- The data which contains in each monthly files were imported into SQL Server.
###### <p>2. Merging Data:</p>
- The data from the 12 tables were merged into one table called the “Annual_trip_data_2024” table. The 'UNION ALL' method is used in this step.  [Click Here](https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/img_sql/1.%20Merge%20Data.sql)
###### <p>3. Manipulate Data: </p>
- Then another new table named “analyze_annual_trip_data” was generated. And it is used to includes additional columns like 'month' , 'day' , 'hour' and 'duration_minutes' to analyse ride frequencies. [Click Here](https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/img_sql/2.%20Manipulate%20Data.sql)


## Analyse Phase:
#### <p> Data Analysing in Microsft SQL Server:</p> 
In this phase the key findings of uncovered data insights which are related to the difference of annual members and casual riders use Cyclistic bikes were analysed by focusing the customer behaviour through analysing the patterns. 
#### SQL Query: [Click Here](https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/img_sql/3.%20Analyze%20Data.sql)

###### <p>•	Percentage of Casual Riders vs Annual Members </p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/img_sql/Percentage%20of%20Casual%20Riders%20vs%20Annual%20Members.png">

###### <p>•	Percentage of Rides per Month </p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/img_sql/Percentage%20of%20Rides%20per%20Month.png">

###### <p>•	Number of Rides per Day</p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/img_sql/Number%20of%20Riders%20per%20Day.png">

###### <p>•	Proportion of Rides by Bike Type </p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/img_sql/Proportion%20of%20Rides%20by%20Bike%20Type.png">

###### <p>•	Percentage of rides per Season</p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/img_sql/Percentage%20of%20Rides%20per%20Season.png">

###### <p>•	Proportion of rides in Each Time Zone </p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/img_sql/Percentage%20of%20Rides%20per%20Time%20Zone.png">

###### <p>•	Frequency of Rides per Hour</p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/img_sql/Frequency%20of%20Rides%20per%20Hour.png">

###### <p>•	Average Ride Duration by Day</p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/img_sql/Average%20Ride%20Duration%20by%20Day.png">


## Share Phase:
#### <p> Data Visualizing in Tableau Public:</p> 
This phase shows the  findings from the analysis which facilitates comparison easily.

###### <p>•	Percentage of Casual Riders vs Annual Members </p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/tableu/Percentage%20of%20Casual%20Riders%20vs%20Annual%20Members.png">
The majority of rides in 2022—59.35% of the total 4,288,562 rides—were made by annual members.

###### <p>•	Percentage of Rides per Month </p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/tableu/Percentage%20of%20Rides%20per%20Month.png">
According to our analysis, annual members routinely log more rides than casual riders throughout all months. Annual members made up the largest percentage of rides in February, accounting for about 82.93% of all rides. However, with about 48.59% of all rides in July, casual riders made up the largest percentage of all rides.

###### <p>•	Number of Rides per Day</p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/tableu/Number%20of%20Rides%20per%20Day.png">
Analysing the daily ride volume reveals some intriguing trends. Annual members routinely have more rides from Monday through Friday than casual riders. Casual riders, however, use the service the most on weekends (Saturday and Sunday), outpacing annual members' ride counts.

###### <p>•	Proportion of Rides by Bike Type </p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/tableu/Proportion%20of%20Rides%20by%20Bike%20Type.png">
Compared to casual riders, a larger share of yearly members use classic bikes, according to the bike types analysis. Furthermore, compared to casual riders, annual members have a stronger preference for electric bikes. But when it comes to parked bikes, casual riders are more likely to use them than yearly members.

###### <p>•	Percentage of rides per Season</p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/tableu/Percentage%20of%20Rides%20per%20Season.png">
When compared to casual cyclists, annual members consistently have the largest percentage of rides across all seasons. Annual members, however, make up the largest percentage during the winter months, making up about 78.99% of all rides. Conversely, casual cyclists make up the largest percentage of rides throughout the summer, accounting for around 46.86% of all rides.

###### <p>•	Proportion of rides in Each Time Zone </p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/tableu/Proportion%20of%20Rides%20in%20each%20Time%20Zone.png">
Among the three time zones—morning, afternoon, and evening—Annual Members use bikes at the highest ratio. In particular, annual members make up roughly 68.15% of rides in the morning time zone, demonstrating their predominance during that time. Casual rides, which make up roughly 50.57% of the rides, outnumber members in the nighttime time zone.

###### <p>•	Frequency of Rides per Hour</p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/tableu/Frequency%20of%20Rides%20per%20Hour.png">
For both annual members and casual riders, the line graph shows clear differences in the number of rides per hour. Notably, the highest utilisation for both rider types occurs at 17:00 (5 p.m.), when annual members log 273,000 rides and casual riders log 167,000.

###### <p>•	Average Ride Duration by Day</p>
<img width="316" alt="3  percentage of rides - result" src="https://github.com/Sewmi-Wijayawickrema/Cyclistic-bike-share-analysis-case-study/blob/main/tableu/Average%20Ride%20Duration%20by%20Day.png">
Compared to annual members, casual cyclists typically ride for far longer periods of time.


## Act Phase:
#### Key takeaways:
###### <p>1. Time Zone Distribution </P>
Casual riders have a larger percentage of rides at night, but annual members are more prevalent in the morning, afternoon, and evening time zones.
###### <p>2. Seasonal Variation</P>
Members have the most rides throughout the year, although the proportion of casual rides is highest in the summer and the fraction of yearly members is largest in the winter.
###### <p>3.	Peak Usage Hour</P>
Annual members have more rides than casual riders, with both groups experiencing peak usage at 5 p.m.
###### <p>4.	Ride Duration</P>
Compared to annual members, casual riders typically bike for longer periods of time.
###### <p>5. Bike Type Preference</P>
Classic and electric bikes are more popular among annual members, whereas docked bikes are more popular among casual riders.
###### <p>6.	Monthly Variation</P>
Throughout every month, annual members routinely log more rides than casual riders. The biggest percentage of casual rides occurs in July, whereas the highest percentage of yearly members occurs in February.
###### <p>7.	Weekday vs. Weekend Usage</P>
Casual riders use the platform more on weekends, whilst annual members often ride more on weekdays.


#### Methods that can be used to increase the number of casual riders who become annual members:
###### <p>1. Customized Membership Plans</P>
rovide yearly membership packages designed especially for docked bike users, offering extra benefits and advantages to promote the switch.
###### <p>2.Enhanced Convenience</P>
To enable longer rides for casual riders and provide extra convenience that persuades them to think about an annual membership, upgrade bike storage facilities, particularly on weekends.
###### <p>3.Marketing Campaigns</P>
To emphasise the benefits of an annual membership and the value it provides to casual riders, start focused marketing efforts during weekends, peak hours, and certain seasons.
###### <p>4.	Targeted Promotions</P>
Emphasise the advantages and financial savings of long-term commitment by providing special discounts or incentives to casual riders who wish to upgrade to yearly memberships.
###### <p>5.Improved Bike Variety</P>
To accommodate casual riders' tastes and improve the riding experience overall, increase the number of vintage and electric bikes in the fleet.

