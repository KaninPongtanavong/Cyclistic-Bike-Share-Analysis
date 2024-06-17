# Cyclistic-Bike-Share-Analysis
This project is a case study which is a part of the Google Data Analytics professional certificate. This project aims to make the learner demonstrate the skills and knowledge acquire throughout the course. We will be performing typical tasks of a junior data analyst while following the steps of the data analysis process: Ask, Prepare, Process, Analyze, Share, and Act. We will be using Jupyter notebook for preparing, processing, and analyzing the data, then we will use Tableau for sharing our findings (we will also perform additional analysis if needed).
![1_sPHAfqCpeT_Hr57CPfVj1Q](https://github.com/get211/Cyclistic-Bike-Share-Analysis/assets/170894868/2f4b97a4-47b8-4ebc-b42a-ec486a85efeb)
## Introduction
In this project, as a junior data analyst working on the marketing analyst team at Cyclistic, we are tasked with analyzing the bike share data. Cyclistic is a bike share company in Chicago that launched in 2016. Since then, it has grown to have more than 5,800 bicycles and 600 docking stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system at any time. Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders, while customers who purchase annual memberships are Cyclistic members.

Cyclistic’s finance analysts have concluded that annual members are much more profitable than casual riders. Although the pricing flexibility helps Cyclistic attract more customers, Moreno, the Director of Marketing, believes that maximizing the number of annual members will be key to future growth. Rather than creating a marketing campaign that targets all-new customers, Moreno believes there is a solid opportunity to convert casual riders into members. She notes that casual riders are already aware of the Cyclistic program and have chosen Cyclistic for their mobility needs. Therefore, the team needs to gain a better understanding of how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics. Moreno and her team are interested in analyzing the Cyclistic historical bike trip data to identify trends. The team will then design a new marketing strategy based on the insights we discover to convert casual riders into annual members. However, Cyclistic executives must first approve our recommendations, so they must be backed up with compelling data insights and professional data visualizations.

## Ask
>The first phrase of the data analysis process is "Ask". In this phrase, we will identify the business task, consider key stakeholders and ask key questions that need to be answered to guide the analysis.

### Business Task
Our main business task is to understand how members and casual riders use Cyclistic bike differently and to identify strategies to convert casual riders into annual members.

### Stakeholders
- Lily Moreno: The director of marketing and your manager. Moreno is responsible for the development of campaigns and initiatives to promote the bike-share program. These may include email, social media, and other channels.

- Cyclistic executive team: The notoriously detail-oriented executive team will decide whether to approve the recommended marketing program.

- Cyclistic marketing analytics team: A team of data analysts who are responsible for collecting, analyzing, and reporting data that helps guide Cyclistic marketing strategy.

### Key Questions
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?

## Prepare
>In the second phrase of the data analysis process, "Prepare", we will gather and organize the data needed for analysis and ensure that the data is reliable, original, comprehensive, current and cited (ROCCC).

The historical data of Cyclistic bike share can be found [here](https://divvy-tripdata.s3.amazonaws.com/index.html). (Please Note: The datasets have a different name because Cyclistic is a fictional company. For the purposes of this case study, the datasets are appropriate and able to answer the business questions. The data has been made available by Motivate International Inc. under this [license](https://divvybikes.com/data-license-agreement).) The datasets are structured data organized as CSV file for each month, we will be using the data of the year 2023 for this project.

After we downloaded all the data from 2023, we inspected it to ensure that it's ROCCC.

The data is provided "AS IS" and is available for the entire year of 2023. It is obtained directly from the source without relying on second or third parties. The data covers all the months of the previous year and has been vetted and made available for public use under the provided license. Although the data contains some missing values, which we will address in the next phase, it is comprehensive enough for our analysis. Hence, it is reliable, original, comprehensive, current, and cited (ROCCC).

There are 13 initial columns present in the dataset including:
- ride_id: Unique identifier for each ride
- rideable_type: Type of bike used
- started_at: Start time of the ride
- ended_at: End time of the ride
- start_station_name: Name of the starting station
- start_station_id: Identifier of the starting station
- end_station_name: Name of the ending station
- end_station_id: Identifier of the ending station
- start_lat: Latitude of the starting station
- start_lng: Longitude of the starting station
- end_lat: Latitude of the ending station
- end_lng: Longitude of the ending station
- member_casual: User type (member or casual)

We then prepare the tool that we are going to use for the next phrase, Jupyter notebook. This include importing all the relevant libraries and the all the CSV file for each month.

## Process
>In the "Process" phrase, we will clean and transform the data for analysis.

We will be using Jupyter notebook for process and analyze phrase. The file can be accessed [here](https://github.com/get211/Cyclistic-Bike-Share-Analysis/blob/main/Cyclistic%20bike-share%20(Process%20%26%20Analyze).ipynb). 

### Merging All the Data
We started by merging all the monthly files into a single DataFrame for 2023. This will allow us to perform a comprehensive analysis. As a result, we have a dataframe of 2023 bike rides that contains 5,719,877 rows in total.

### Data Cleaning
After merging the data, we will performed the following steps to clean our data:
* Removing missing values: We removed all rows that containing a Nan values, as a result there are 4,331,707 rows left.
* Removing duplicate values: We verified that there are no duplicate values in our dataframe.
* Correcting Data Type: We inspected the data types of each column to ensure they are suitable for analysis. For instance, we converted the data types of started_at and ended_at to datetime object.

### Data Transformation
We then created new columns using the existing data. This included:
* Extracting the day, month, and time from the started_at column.
* Calculating ride duration for each ride.
* Calculating the distance for each ride.
* Categorizing the type of ride as 'One-way trip' or 'Round trip'.
* Categorizing each ride as 'Weekend' or 'Weekday'.
* Categorizing each ride by season, including 'Winter', 'Spring', 'Summer', 'Fall'
* Categorizing each ride by part of the day as 'Midnight', 'Morning', 'Afternoon', 'Evening' or 'Night'
* Renaming the column for more appropriate names, such as 'member_casual' to 'user_type'

### Filtering Data
After transforming the data, we inspected it again to ensure data integrity. We found that some rows contained negative ride durations. We filtered out those rows, resulting in 4,331,641 rows.

## Analyze
> After processing our data, we will analyze the cleaned and transformed data to uncover insights and trends.

We will use the processed data to explore patterns and trends that will help us answer the key business questions.
### Summary of Analysis
* There are a total of 4,331,641 rides in 2023
* The average riding distance is 2.065 km.
* The average ride duration is 15.95 minutes.
* 64.64% of the rides are by member riders (2,799,920 rides)
* 35.36% of the rides are by casual riders (1,531,721 rides)
* There are two types of trip: one-way trips and round trips
  * 95.85% of the total rides are one-way trips (4,151,792 rides) and 4.15% are round trips (179,849 rides).
* There are three types of bikes: classic, docked, and electric
    * 2,690,707 rides used classic bikes
    * 76,124 rides used docked bikes
    * 1,564,810 rides used electric bikes
* Summer is the season that saw the highest number of rides, totaling 1,693,622 rides. August has the highest number of rides in summer, totaling 584,912 rides.
* 3,108,242 rides occurred on weekdays and 1,223,399 rides on weekends, which is equivalent to 71.76% and 28.24%, respectively.
* The part of the day with the highest total number of rides is the afternoon, but the peak hour is 17:00.
* Top 3 starting stations overall:
  1. Streeter Dr & Grand Ave with the total of 59,614 rides (43,370 casual, 16,244 member)
  2. DuSable Lake Shore Dr & Monroe St with the total of 38,014 rides (28,714 casual, 9,300 member)
  3. Michigan Ave & Oak St 34,780 rides with the total of (21,098 casual, 13,682 member)

### Analysis of Member Riders
* Number of rides by member riders = 2,799,920 rides.
* The average ride distance is 2.038 km.
* The average ride duration is 12.13 minutes.
* 97.28% of the rides are one-way trips (2,732,635 rides) and 2.72% are round trips (76,285 rides).
  * The average ride distance and duration for member riders that use the bike for one-way trips are 2.095 km and 11.99 minutes, respectively.
  * The average ride duration for members that use the bike for round trips is 17.26 minutes.
* Member riders never used docked bikes in 2023.
* 1,817,702 rides used classic bikes.
  * The average ride distance and duration for members using classic bikes are 1.897 km and 13 minutes, respectively.
* 982,218 rides used electric bikes.
  * The average ride distance and duration for members using electric bikes are 2.298 km and 10.53 minutes, respectively.
* For members, summer is the season with the highest number of rides, totaling 994,686 rides. August is the month in summer with the highest number of rides, totaling 351,061 rides.
* 76.48% of member rides occurred on weekdays and 23.52% on weekends, which is equivalent to 2,141,419 and 658,501 rides, respectively.
* The afternoon is the part of the day that has the highest number of rides, but the peak hour is 17:00.
* Top 3 starting stations for members:
  1. Clinton St & Washington Blvd: 24,299 rides
  2. Kingsbury St & Kinzie St: 24,214 rides 
  3. Clark St & Elm St: 23,079 rides

### Analysis of Casual Riders
* Number of rides by casual riders = 1,531,721 rides.
* The average ride distance is 2.114 km.
* The average ride duration is 22.94 minutes.
* 93.24% of the rides are one-way trips (1,428,157 rides) and 6.76% are round trips (103,564 rides).
  * The average ride distance and duration for casual riders that use the bike for one-way trips are 2.267 km and 21.35 minutes, respectively.
  * The average ride duration for casual riders that use the bike for round trips is 44.82 minutes.
* 873,005 rides by casual riders used classic bikes.
  * The average ride distance and duration for casual riders that use classic bikes are 2.071 km and 25.75 minutes, respectively.
* 79,124 rides by casual riders used docked bikes.
  * The average ride distance and duration for casual riders that use docked bikes are 2.155 km and 53.98 minutes, respectively.
* 582,952 rides by casual riders used electric bikes.
  * The average ride distance and duration for casual riders that use electric bikes are 2.173 km and 14.66 minutes, respectively.
* For casual riders, summer is the season with the highest number of rides, totaling 698,936 rides. August is the month in summer with the highest number of rides, totaling 233,851 rides.
* 63.12% of casual rides occurred on weekdays and 36.88% on weekends, which is equivalent to 966,823 and 564,898 rides, respectively.
* The afternoon is the part of the day that has the highest number of rides, but the peak hour is 17:00.
* For casual riders, the month with the highest number of rides is July.
* Top 3 starting stations for casual riders:
  1. Streeter Dr & Grand Ave: 43,370 rides
  2. DuSable Lake Shore Dr & Monroe St: 28,714 rides
  3. Michigan Ave & Oak St: 21,098 rides

### Additional Findings
* The average ride duration by bike type:
  * Classic bikes = 17.14 minutes
  * Docked bikes = 53.98 minutes
  * Electric bikes = 12.07 minutes
* The average ride distance by bike type:
  * Classic bikes = 1.953 km
  * Docked bikes = 2.155 km.
  * Electric bikes = 2.252 km.
* Winter is the season that has the lowest number of rides, both the 2022-2023 winter (January, February) and 2023-2024 winter (December). The first winter (2022-2023) had 77,965 rides, and the second winter (2023-2024) had 39,638 rides.
* On weekdays, the number of rides peaks at 7:00 and 8:00 in the morning. The number of rides then drops slightly and starts rising again from 11:00, peaking at 17:00 with 364,651 rides, 255,272 of which were by members.
* On weekends, the number of rides rises steadily from 4:00 in the morning until after 16:00, after which the number of rides starts to drop.
* Member riders are more evenly distributed across the city, indicating regular, everyday use.
* Stations near tourist attractions such as Navy Pier are significantly more popular among casual riders.

## Share
> In the "Share" phase, we present our findings through visualizations and summaries to ensure the insights are clear and actionable.

We have created an interactive Tableau dashboard to visualize our findings. We set up actions, filters, and additional information in the tooltips to enhance the audience's interaction with the data. You can access the dashboard [here](https://public.tableau.com/views/CyclisticBike-ShareAnalysisGoogleDataAnalyticsProject/Dashboard?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link)

![Dashboard](https://github.com/get211/Cyclistic-Bike-Share-Analysis/assets/170894868/ee87280b-c3d9-4158-b862-957fd2993896)

### Filtered Dashboard Views
We have include a few filtered views of the dashboard to highlight specific insights:

**Dashboard Filtered by User Type (Members)**

![Dashboard(member)](https://github.com/get211/Cyclistic-Bike-Share-Analysis/assets/170894868/80d99cf3-beab-494c-891c-da88326eeda2)

**Dashboard Filtered by User Type (Casual)**

![Dashboard(casual)](https://github.com/get211/Cyclistic-Bike-Share-Analysis/assets/170894868/9066bde5-ce0f-453e-837c-5da5d72b148c)

**Dashboard Filtered by Ride Type (One-Way Trip)**

![Dashboard(one-way)](https://github.com/get211/Cyclistic-Bike-Share-Analysis/assets/170894868/955c68d5-5117-448b-96aa-e83daceee65c)

**Dashboard Filtered by Ride Type (Round Trip)**

![Dashboard(round)](https://github.com/get211/Cyclistic-Bike-Share-Analysis/assets/170894868/37c64490-9b13-40ed-bbf9-55f7c94fca43)

**Dashboard Filtered by Bike Type (Docked Bike)**

![Dashboard(docked bike)](https://github.com/get211/Cyclistic-Bike-Share-Analysis/assets/170894868/16914425-4ad7-47fa-84a5-7a5e3de5ae2e)

**Dashboard Filtered by Top 10 Starting Station (Streeter Dr & Grand Ave)**

![Dashboard(map)](https://github.com/get211/Cyclistic-Bike-Share-Analysis/assets/170894868/58f784c5-496a-4dbc-8c2c-718656d860d7)

### Conclusions

