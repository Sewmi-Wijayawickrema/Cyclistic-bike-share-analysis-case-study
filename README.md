# Cyclistic-bike-share-analysis-case-study
### Analysis of Cyclistic bike-share data to identify trends and improve customer conversion.
<p align="center">
<img width="519" alt="Capture" src="'/Users/sewmiwijayawickrema/Downloads/1*btecI8i1yNczHsGP3z_sCg.webp'">
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
<p>• Question 1: How do annual members and casual riders use Cyclistic bikes differently?
  </p>
<p>• Answer :</p>
In this phase, the analysis will be guided by the following questions to realize how annual members and casual riders use Cyclistic bikes differently. 
<p> </p>
<p>•	Percentage of Casual Riders vs Annual Members </p>
<p>•	Percentage of Rides per Month </p>
<p>•	Number of Rides per Day</p>
<p>•	Proportion of Rides by Bike Type </p>
<p>•	Percentage of rides per Season</p>
<p>•	Proportion of rides in Each Time Zone </p>
<p>•	Frequency of Rides per Hour</p>

## Prepare Phase:
The following analysis is made up of monthly files for March 2024 through Feb 2025 which consists the latest data of the past 12 months. 
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
- The data from the 12 tables were merged into one table called the “Annual_trip_data_2024” table. The 'UNION ALL' method is used in this step.  SQL Query:**** 
###### <p>3. Manipulate Data: </p>
- Then another new table named “analyze_annual_trip_data” was generated. And it is used to includes additional columns like 'month' , 'day' , 'hour' and 'duration_minutes' to analyse ride frequencies. SQL Query:**** 


## Analyse Phase:
#### <p> Data Analysing in Microsft SQL Server:</p> 
In this phase the key findings of uncovered data insights which are related to the difference of annual members and casual riders use Cyclistic bikes were analysed by focusing the customer behaviour through analysing the patterns. 

###### <p>•	Percentage of Casual Riders vs Annual Members </p>
###### <p>•	Percentage of Rides per Month </p>
###### <p>•	Number of Rides per Day</p>
###### <p>•	Proportion of Rides by Bike Type </p>
###### <p>•	Percentage of rides per Season</p>
###### <p>•	Proportion of rides in Each Time Zone </p>
###### <p>•	Frequency of Rides per Hour</p>




## Share Phase:
#### <p> Data Visualizing in Tableau Public:</p> 
This phase shows the  findings from the analysis which facilitates comparison easily.

###### <p>•	Percentage of Casual Riders vs Annual Members </p>
###### <p>•	Percentage of Rides per Month </p>
###### <p>•	Number of Rides per Day</p>
###### <p>•	Proportion of Rides by Bike Type </p>
###### <p>•	Percentage of rides per Season</p>
###### <p>•	Proportion of rides in Each Time Zone </p>
###### <p>•	Frequency of Rides per Hour</p>

## Act Phase:
#### Key takeaways:
###### <p>1. Time Zone Distribution </P>
###### <p>2. Seasonal Variation</P>
###### <p>3.	Peak Usage Hour</P>
###### <p>4.	Ride Duration</P>
###### <p>5. Bike Type Preference</P>
###### <p>6.	Monthly Variation</P>
###### <p>7.	Weekday vs. Weekend Usage</P>

#### Strategies that can proceed to convert more Casual Riders into Annual Members:
###### <p>1. Customized Membership Plans</P>
###### <p>2.Enhanced Convenience</P>
###### <p>3.Marketing Campaigns</P>
###### <p>4.	Targeted Promotions</P>
###### <p>5.Improved Bike Variety</P>


