# Cyclistic-Bike-Share-Analysis
This project is a case study which is a part of the Google Data Analytics professional certificate. This project aims to make the learner demonstrate the skills and knowledge acquire throughout the course. We will be performing typical tasks of a junior data analyst while following the steps of the data analysis process: Ask, Prepare, Process, Analyze, Share, and Act. We will be using Jupyter notebook for preparing, processing and analyzing the data, then we will use Tableau for sharing our finding (we will also perform additional analysis if needed).

![1_sPHAfqCpeT_Hr57CPfVj1Q](https://github.com/get211/Cyclistic-Bike-Share-Analysis/assets/170894868/2f4b97a4-47b8-4ebc-b42a-ec486a85efeb)
## Introduction
In this project, as a junior data analyst working on the marketing analyst team, we are tasked with analyzing the Cyclistic bike share data. Cyclistic is a bike share company in Chicago that launched in 2016. Since then, it has grown to have more than 5,800 bicycles and 600 docking stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system at any time. Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders, while customers who purchase annual memberships are Cyclistic members.

Cyclistic’s finance analysts have concluded that annual members are much more profitable than casual riders. Although the pricing flexibility helps Cyclistic attract more customers, Moreno, the Director of Marketing, believes that maximizing the number of annual members will be key to future growth. Rather than creating a marketing campaign that targets all-new customers, Moreno believes there is a solid opportunity to convert casual riders into members. She notes that casual riders are already aware of the Cyclistic program and have chosen Cyclistic for their mobility needs. Therefore, the team needs to gain a better understanding of how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics. Moreno and her team are interested in analyzing the Cyclistic historical bike trip data to identify trends. The team will then design a new marketing strategy based on the insights we discover to convert casual riders into annual members. However, Cyclistic executives must first approve our recommendations, so they must be backed up with compelling data insights and professional data visualizations.

## Ask
>The first phrase of the data analysis process is "Ask". In this phrase, we will identify the business task, consider key stakeholders and ask key questions that need to be answered to guide the analysis.

### Business Task
Our main business task is to understand how members and casual riders use Cyclistic bike differently and to identify strategies to convert casual riders into annual members.

### Stakeholders
● Lily Moreno: The director of marketing and your manager. Moreno is responsible for the development of campaigns and initiatives to promote the bike-share program. These may include email, social media, and other channels.

● Cyclistic executive team: The notoriously detail-oriented executive team will decide whether to approve the recommended marketing program.

● Cyclistic marketing analytics team: A team of data analysts who are responsible for collecting, analyzing, and reporting data that helps guide Cyclistic marketing strategy.

### Key Questions
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?

## Prepare
>In the second phrase of the data analysis process, "Prepare", we will gather and organize the data needed for analysis and ensure that the data is reliable, original, comprehensive, current and cited (ROCCC).

The historical data of Cyclistic bike share can be found [here](https://divvy-tripdata.s3.amazonaws.com/index.html). (Please Note: The datasets have a different name because Cyclistic is a fictional company. For the purposes of this case study, the datasets are appropriate and will enable you to answer the business questions. The data has been made available by Motivate International Inc. under this [license](https://divvybikes.com/data-license-agreement).) The dataset are organized as CSV file for each month, we will be using the data of the year 2023 for this project.

After we downloaded all the data from 2023, we inspected it to ensure that it's ROCCC.

**R**eliable: The license states that "THE DATA IS PROVIDED “AS IS,” AS AVAILABLE," and we can collect the data for the entire year of 2023, making it reliable and complete.

**O**riginal: The datasets are obtained from the original source, meaning we are not relying on second or third parties.

**C**omprehensive: The data contains some missing values, which we will address the issue in the next phrase.

**C**urrent: The datasets are relavent as it contains the data from all the month of the previous year.

**C**ited: The datasets have been vetted and provided for public use under this [license](https://divvybikes.com/data-license-agreement)
