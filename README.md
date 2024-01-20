# Converting Casual Riders to Annual Members 


### Scenario
We are a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations.

### Business Task
The goal of this case study is to provide clear insights for designing marketing strategies aimed at converting casual riders into annual members. Towards this goal, I asked the following questions:

How do annual members and casual riders use Cyclistic bikes differently?

Why would casual riders buy Cyclistic annual memberships?

How can Cyclistic use digital media to influence casual riders to become members?


### Data Preperation
This case study uses Cyclistic's historical trip data (previous 12 months) to analyze and identify trends. The data has been made available by Motivate International Inc. under and open license. The data can be dowloaded [here.](https://divvy-tripdata.s3.amazonaws.com/index.html)

This data is reliable, original, comprehensive and current as it is internally collected and stored safely by Cyclistic from January 2022 to December 2022. Personally identifiable information  such as credit card numbers has been removed because of data-privacy issues.

The data selected for use covers the last 12 months. Each month has a separate dataset. The datasets are organized in tabular format and have 13 identical columns. Combined, the datasets have 4073561 uncleaned rows. The **member_casual** column will allow me to group, aggregate and compare trends between casual riders and member riders. 

### Cleaning the Data 
The tools I used to clean and process the data were Excel and BigQuery. If I were to do this project again I would opt out of using excel and go straight into BigQuary, reason being A worksheet can only have 1,048,576 rows in Microsoft Excel because of its inability to manage large amounts of data. Because the Cyclistic dataset has more than 5.6 million rows, it is essential to use a platform like BigQuery that supports huge volumes of data. Never the less I opted into using power query in excel and combined all 12 sheets into a singular sheet. I filtered the sheet to check if all ride_ids were unique and had a length of 16. I then filtered out rows that returned null or 0 values on all columns of the spreadsheet. after I loaded the powerquery into a new excel sheet and titled it 2022Bikedata.csv.

### Transforming the Data 
Using Bigquery I loaded in my 2022Bikedata.csv to create new insights from my dataset I created 3 new columns:

Total_time_used : Getting the difference between the ended_at and started_at columns. This yielded a timedelta object which I converted to seconds then minutes.
day_of_the_week & month: Using the started_at column to extract the date
hour_used: Using the started_at column to extract the hour

### Analyzing the data 
In this step, I analyzed the cleaned data to find out how annual members and casual riders use Cyclistic bikes differently.

First, I got the total number of bike hired and established how they were shared between casual riders and member riders. Next, I examined how total bike hires were distributed per month and then per day. This revealed some interesting trends that I shall discuss in the share stage.

Next, I examined how bike hires between the two types of rider categories compared in a given month of the year and day of the week. The goal at this point was to find out whether casual riders had a preference for certain days or months compared with member riders.

Next, I wanted to compare the difference in average ride length between casual riders and member riders. I discovered that casual riders tend to ride for longer periods of time compared to member riders. I was intrigued and decided to explore how the average ride length compares for both rider categories on daily and monthly basis.

Finally I compared how the type of bike hired compared between the two rider categories.

### Sharing Insights
I created visualizations using tableau to communicate the results of my analysis. the dashboard can be found here
https://public.tableau.com/app/profile/jace.chua/viz/Cyclistic2022data/Dashboard1 

After identifying the differences between casual and member riders, marketing strategies to target casual riders can be developed to persuade them to become members.
Recommendations:

Marketing campaigns might be conducted in spring and summer at tourist/recreational locations popular among casual riders.
Casual riders are most active on weekends and during the summer and spring, thus they may be offered seasonal or weekend-only memberships.
Casual riders use their bikes for longer durations than members. Offering discounts for longer rides may incentivize casual riders and entice members to ride for longer periods of time.

