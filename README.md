# Divvy - Data Analysis project:
The Divvy Project focus on utilizing bike ride data **(as of July-2024)** to produce meaningful actions for Divvy - a bike sharing company in Chicago - on improving their electric bike leasing to non-member customers which help increase the opportunity to convert them to members.
Presentation is at: [https://tinyurl.com/powerBI-DivvyAnalysis]

## Key findings:
**1. Overview and problem:**
- While the performance over the last 12 months of Divvy is stable with 5.3 million rides (equal to performance of previous same period), there has been a 10% decline in terms of e-bike rides which is the main revenue driver of the company.

**2. Why:**
- The decline mainly comes from casual/ non-member users segment which has seen decline in both number and length of e-bike rides.

- Considering the fact that over the last 2 years, Divvy has not recover to its 2022 peak during the high-demand summer seasons, it is worth taking a look into how to improve the performance of non-member riders.
  
- Taking a look into pricing for non-members, it can been seen that over the past 2 years, price for 15-min ride has increased by 20% on a single ride ticket, and a day pass price increase by over 30% -> This can be seen as a factor hinder more and longer rides from these non-members.

**3. How:**
- By their behaviors, it is seen that while members' rides occur over the course of weekdays and slightly decline during weekend, non-members seem to take Divvy bike for their exploratory experience during the weekend which show the peak during the weekend.

- Considering the peak hours in which there can be high demand for rides, Divvy can implement promotional campaigns to encourage non-members on taking more rides.
  
- The focus time would be commute time during weekday (7-9AM and 4-6PM), lunch and afternoon time during weekend (11AM-3PM)
- Beside knowing when to promote, where to promote is also important:
  - West Loop, River North, Lake View, Lincoln Park are 4 key areas during weekday
  - Lake View, Lincoln Park are the focus for weekend.

# About the project:

This is my data analysis portfolio project with the end-to-end workflow of 3 steps:
1. Data collection: 
2. Data cleaning & Exploratory analysis:
3. Data visualization and Insights presentation: 

## 1. Data collection:
### 1.1. Bike ride dataset:
The bike ride dataset is collected through open source data directly from Divvy - a bike sharing platforms based in Chicago, Illinois, USA. 

The source is at: [https://divvybikes.com/system-data]


### 1.2. Station dataset:
Beside the main bike ride dataset, the information about stations' location and capacity is also obtained through The City of Chicago's open data portal which is a great source for information related to the city's neighborhoods, facilities,etc.

Link to the station dataset: [https://data.cityofchicago.org/Transportation/Divvy-Bicycle-Stations-Map/bk89-9dk7]


### 1.3. Chicago map:
During my data cleaning process, I came up with an interesting idea whether I can map out the location of each bike ride on the map of Chicago city to know which area has the most rides, and how Divvy can focus on these areas to attract more users. 
The shape map of Chicago is also collected through The City of Chicago's open data portal at: [https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-Neighborhoods/bbvz-uum9]


## 2. Data cleaning and Exploratory analysis:

This step focus on understand the data and deriving other measures that can be useful for analysis.
I used pandas libraries for cleaning and exploring the dataset, the notebook can be found here: [https://github.com/sillykiddo-99/Divvy-bike-sharing-analysis/blob/main/divvy_cleaning.ipynb]

### 2.1 Understand the data:
The bike rides dataset consist of 12 columns, covering:
- The type of the ride (e-bike, classic bike, docked bike)
- The detailed start & end date, time, stations

### 2.2 Data cleaning:
#### Adding calculated column:
- Adding distance of each trip using math library and Haversine formula to calculate the distance of 2 points based on their longitude and latitude
- Adding the stating and ending time columns of each ride
- Adding the ride length by calculating difference of start and end time
- Adding month, year, day_of_week column, time_hr columns

#### Clean outliers
- Clean out rows that have end time before start time
- Clean out rows that have outliers riding time using the boxplot and Inter quartile range (IQR) method

#### Map out neighborhoods
- Using geojson dataset to map the neighborhoods to each row in bike ride and stations dataset

### 2.3 Data exploratory:
#### Bike ride characteristics:
- There are 5.3 million rides over the last 12 months
- By seasonality, summer months (May - August) have highest number of rides in L12Ms
- By time of day, 7-9AM and 4-6PM are the 2 most popular time for rides
- By weekday, Saturday is the day that has the most ride
- Currently, there are 999 stations
- ...

#### Customer behaviors:
- About 33% are classic rides, and 67% are electric bike rides
- Average trip length of e-bike is 10 mins, classic bike is about 12 mins
- ....


## 3.Data visualization and Insights presentation:
For Power BI interactive mode, please visit here: [https://tinyurl.com/powerBI-DivvyAnalysis]

For PDF presentation, please visit here: [https://github.com/sillykiddo-99/Divvy-bike-sharing-analysis/blob/main/Divvy%20Data%20Analysis%20Project.pdf]
