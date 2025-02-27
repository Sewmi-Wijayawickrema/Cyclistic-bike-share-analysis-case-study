# Cyclistic-bike-share-analysis-case-study
Analysis of Cyclistic bike-share data to identify trends and improve customer conversion.
 ### Data Source: [divvy_tripdata](https://divvy-tripdata.s3.amazonaws.com/index.html)
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
This stages would be applied in this case study. 

## Data Analysis Process
### Ask Phase:
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

### Prepare Phase:
<p> </p> <p>• </p>
The following analysis is made up of monthly files for March 2024 through Feb 2025 which consists the latest data of the past 12 months. 
After extracting all 12 files using *Excel, the table is consisted of thirteen columns pertaining to the bike trips.
And the coloumns issue data on the ride ID, rideable type, start and end station ID’s and locations, coordinates, and membership type for each sheet.


### Process Phase:

##### <p>•	Data Cleaning in Excel: 
The dataset was refined, inconsistencies were addressed, and the ride length information was formatted appropriately for subsequent analysis after cleaning data.</p>

###### <p>• Checking for Duplicates:
The duplicate values were searched and then removed using through the “Remove Duplicates” feature in Excel. This helped ensure data integrity and eliminate any duplicated entries if there are any.</p>
###### <p>• Validating Column Values:
The values in some specific columns, such as 'rideable_type' and 'member_casual', are verified to make sure the consistency and accuracy of the data set. Valid values such as 'classic_bike', 'docked_bike', 'electric_bike' for 'rideable_type', and 'casual_member' for 'member_casua', were retained to validate data.</p>
###### <p>• Removing Blank Values:
All columns were checked for incomplete or blank values. Rows with missing values (like start_station_name,end_station_name, start_station_id and end_station_id) were removed to clarify the completeness of data.</p>
###### <p>• Removing Unwanted Columns: 
Columns start_lat,end_lat, start_lng and end_lng are not relevant to the given analysis. Therefore, those were removed from each file to focus only on the relevant variables.</p>
###### <p>• Adding the Ride Length Column:
A new column which is named as “ride_length” was added and it was used to calculate the duration of each ride. The values of the column were acquired by subtracting started_at timestamp from ended_at timestamp.</p>
###### <p>• Setting the Time Format:
The “Format > Cells > Time > 37:30:55” method was used to format the ride_length according to “HH:MM:SS”. It is to clarify that the ride duration was given in standardized format.</p>
###### <p>• Applying Conditional Formatting:
To highlight ride lengths that fell outside the desired range, conditional formatting was applied to the ride_length column. If a ride length is less than one minute or greater than 24 hours, they were formatted differently, to easily identify for further analysis.</p>
###### <p>• Sorting the Table:
To keep data consistency the table was sorted in ascending order based on the started_at column.</p>

##### <p>•	Data Transformation in SQL: </p>

###### <p>• Importing Data: </p>
###### <p>• Merging Data:</p>
###### <p>• Manipulate Data: </p>
###### <p>• </p>

### Analyse Phase:
### Share Phase:
### Act Phase:
