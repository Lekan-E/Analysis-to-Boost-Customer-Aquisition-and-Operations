# Customer and Product Analysis using Machine Learning

## Project Background
Cyclistic is a bike-sharing company that offers access to over 9000+ bikes and 600+ stations across Chicago, providing a flexible and cost-effective solution for casual riders and annual member.

The company recorded over 5 million trips in the past year and are looking to capitalize on this data to improve operational efficiency, marketing efforts, resource allocation, and understand customer preferences and behaviour. This project thoroughly analyzes and synthesizes this data using various data analytical tools and Machine Learning alogrithm in order to uncover critical insights that will improve business process and boost membership conversion.

Insights and recommendations are provided on the following key areas and departments:

* **Sales Trends Analysis**: Evalutation of sales patterns, both members and casual riders, focusing on Revenue, Ride Volumne and Revenue per Ride.
* **Product Level Performance**: An analysis of Cyclistic's various bike types, understanding user's perference and their impact on the number of rides, trip duration and the revenue generated.
* **Optimize Staffing and Maintenance**: An assessment to improve operations efficiency by adjusting staffing and maintenace schedules to align with peak user demands.
* **Seasonal and Holiday Marketing Campaigns**: A seasonal analysis to offer discounts and loyalty incentives to boost ridership and membership conversion by capitalizing on timed periods.
* **Targeted Marketing and Customer Engagement**: An analysis for the marketing team, that targets campaigns at key time of the day and high-traffic regions designed to boost conversion.

The Python Jupyter notebook utilized to clean, prepare and extract data can be found here.

The Python Jupyter notebook to analyze the data using self-guided questions can be found here.

An interactive monthly Tableau dashboard can be found [here](https://public.tableau.com/app/profile/lekanelegbede/viz/HRDailyRidesDashboard/RideDashboard).

Daily ride trackers can be found [here]()

## Data Structure & Final Data
Cyclistic database structure as seen below consists of a single table with a total row count of 5,300,458 rides.

To gain deeper insights, we need to collect/extract the following data:
* Holiday Dates - Via webscraping we extracted the dates and events for the whole year
    - Source: https://www.timeanddate.com/weather/usa/chicago/historic?month=1&year=2021
* Weather: Collect hourly data for each day with over 8,785 records.
    - Source: (PAID) https://www.visualcrossing.com/weather/weather-data-services/Chicago,United%20States/metric/2020-12-01/2021-11-30

![Alt Text](https://github.com/Lekan-E/Customer-and-Product-Analysis-using-ML/blob/9719f429419f7dddcc29019b758d4dd613a80558/Images/Misc/drawSQL-image-export-2024-09-27.png)

Prior to beginning the analysis, a variety of data cleaning checks were conducted using statistical techniques for data accuracy and using the pricing schema from BIKE SHARE TORONTO to calculate trips revenue. The Python notebooks to inspect and perform quality checks can be found here.


## Executive Findings
Overview of Findings

## Business Task
The business problems are the following:
* Geospatial Analysis using K-Means Clustering - Create station clusters to identify and group the different stations based on number of rides using the insights gained will aid in planning for station expansion, upgrades and many more.
    * Achieve an Inertia as close to 0 as possible and Silhoutte score as close to 1 to determine a sutiable K value.
* Outliers Detection and Analysis - Investigate the outliers in the dataset and analyze the possible causes and provide recommendations.
* Descriptive Analysis - To understand annual member and casual riders/customers behaviour and preference, i.e the number of trips taken, trip duration, bike type, time and days, start and end stations.
* Provide recommendations to convert casual riders to annual members.

<br />

## Dataset
The data was collected from a Google capstone project on a month-month basis for a year, stored as a csv file.

## Feature Engineering and Selection
In order to utilise as much possible data, we need to perform the following:
* Get total number of rides from each station
* Extract the daily peak period (Morning, Afternoon, Night) from the ride start time.

## Model Selection and Training
A range of algorithmns were selected from the scikit-learn library, including K-Means Nearest Neighbour and DBSCAN.

## Methodology
### Python Libraries
The libraries used in this project include:
* Pandas – For storing and manipulating structured data. Pandas functionality is built on NumPy
* Numpy – For multi-dimensional arrays, matrix data structures and, performing mathematical operations
* Matplotlib and Seaborn – For all visualizations (including maps and graphs)
* Scikit learn - For Machine Learning tasks

- Tableau for Visualization

# Summary of Insights
## Station Clusters:
Using k-means clustering algorithm, we can easily identify and cluster the stations into 4 different group based on customer usage. An ineractive Tableau dashboard can be found here, it gives more context to the stations in each cluster and the number of rides from each station during that time period.

![Alt Text](https://github.com/Lekan-E/Customer-and-Product-Analysis-using-ML/blob/06788a030db97e051c6d8285381117158fbbcf9f/Images/Misc/Start%20Station%20Cluster.png)

### Summary
The station clustering results reveal four distinct clusters, each characterized by the total number of rides and the number of stations within each cluster. Here's a detailed breakdown:

- Cluster 0 [Orange]
Total Ride Count: 1,559,880
Number of Stations: 562
Average Rides per Station: 2,776
- Cluster 1 [Green]
Total Ride Count: 142,720
Number of Stations: 38
Average Rides per Station: 3,755
- Cluster 2 [Brown]
Total Ride Count: 3,507,239
Number of Stations: 189
Average Rides per Station: 18,559
- Cluster 3 [Purple]
Total Ride Count: 103,583
Number of Stations: 57
Average Rides per Station: 1,817


### Insights:
- Cluster 2 has the highest total ride count and the highest average rides per station, indicating that these stations are the most popular and heavily used in the bike-sharing network.
- Cluster 0 has a substantial total ride count but spread across a large number of stations, suggesting moderate usage across many stations.
- Cluster 1 has relatively fewer stations but a higher average rides per station than Cluster 0, pointing to more concentrated usage at these stations.
- Cluster 3 shows the lowest total ride count and average rides per station, indicating these stations are the least used in the network.
- Clustered Usage: Several stations (e.g., Wells St & Hubbard St, Wells St & Concord Ln, Wells St & Elm St) appear frequently in the top lists, indicating concentrated areas of high bike usage in certain regions.


### Recommendations & Next Steps 

Implications for Bike-Sharing Operations:
- Cluster 2 stations might require more maintenance and frequent bike rebalancing due to high usage.
- Cluster 0 and Cluster 1 stations might benefit from targeted promotions or infrastructure improvements to balance the load and potentially increase usage.
- Cluster 3 stations may need further investigation to understand the low usage and explore ways to enhance their attractiveness or accessibility.

## Members-Ride Analysis
Analyzing trips and member trends from November 2020-2021. Interactive Tableau dashboard can be found here.
Stakeholder Dashboard:

![Alt Text](https://github.com/Lekan-E/Comparative-Analysis-Project/blob/main/Images/Dashboard/Main%20Dashboard.png)

### Insights:
#### Monthly Observation
- There is a clear seasonal pattern in the usage of the bike-sharing service. Both casual and member rides significantly increase during the warmer months (May to September) and decrease during the colder months (November to February).
- The peak usage for both casual and member riders occurs in the summer months, particularly in July and August.
- There is a noticeable drop in the number of rides during the winter months (December to February). This decline is more pronounced for casual riders compared to members.
#### Weekly Observations
- Weekend Usage: Casual riders show significantly higher usage on weekends, with Saturday being the peak day. This suggests that casual riders are likely using the bikes for leisure and recreational purposes.
- Member Usage: Member riders exhibit a more consistent and high usage pattern throughout the week, with a notable peak on Wednesday. This indicates that members might be using the bike-sharing service for regular commuting.
- Weekday Preferences: Members have high usage on Tuesday, Wednesday, Thursday, and Friday, reflecting a preference for using the service during workdays, likely for commuting.
- Peak Usage: Both casual and member riders prefer biking in the afternoon, making it the busiest time of the day.
- Member Riders: Have a consistent and high usage pattern throughout the day, with a notable peak in the afternoon. Morning and night times also see significant usage, reflecting potential commuting patterns.
- Casual Riders: Show a strong preference for afternoon and night rides, indicating leisure or non-commuting uses. Morning rides are less frequent compared to other times.

#### Bike Preference
- Classic Bikes: Most used bike type for both casual and member riders, with members showing a strong preference.
- Docked Bikes: Least popular among all types, with significantly lower usage, particularly by members.
- Electric Bikes: Moderately popular, with higher usage by members. Their popularity indicates a growing trend towards electric bikes for convenience and speed. 

### Recommendations:
#### Monthly Recommendations
- Targeted Marketing: Marketing efforts can be intensified in the spring to attract both casual and potential member users in preparation for the peak summer months.
- Organize community events and bike rides during the spring and summer months to boost engagement and attract more casual users.
- Highlight the benefits of membership during the winter months to encourage casual users to become members, ensuring more stable usage throughout the year.
#### Weekly Recommendations
- Offer promotions and discounts specifically aimed at casual users on weekdays to balance the usage patterns and increase ridership during these days.
- Implement loyalty programs or additional perks for members to encourage continued usage, especially on weekends.
- Organize events or partner with local attractions and businesses on weekends to attract more casual users and potentially convert them into members.


## Outliers Analysis
Outliers are critical data points that deviate significantly from the majority of data. Analyzing these outliers provides insights into potential data quality issues and unusual usage patterns. Our bike-sharing dataset contains 423,944 rows with outlier values, accounting for 7.39% of the total dataset. The analysis reveals that outliers in ride duration are predominantly from casual users, who not only account for the majority of outlier rides but also tend to have longer rides on average compared to members.
![Alt Text](https://github.com/Lekan-E/Analysis-for-a-Bike-Sharing-Company-using-Machine-Learning/blob/c7d6ad96281ad9c300141f6bd78e07391e5e6610/Images/Misc/Ride%20Duration.png)

### Insights
- Casual Riders: The discrepancy suggests that while the average casual ride duration is much lower, there are a few exceptionally long rides. These outliers could be due to special circumstances or rare usage patterns.
- Members: Similarly, members also have a small number of exceptionally long rides, though their typical ride duration is shorter than that of casual riders. The long outlier rides for members may indicate different usage patterns or behaviors not captured by the typical ride duration.

In summary, outliers have ride durations that are several times longer than the typical ride durations for both casual riders and members. This information can be useful for understanding rare but significant usage patterns

Classic bikes have the highest number of outliers, with 204,274 rides. In comparison, docked bikes and electric bikes have fewer outliers, with 110,820 and 108,850 rides, respectively. This indicates that classic bikes might have a higher rate of issues or anomalies in the dataset compared to docked and electric bikes. This could be due to several factors, such as:
- Usage Patterns: Classic bikes might be used more frequently or in different conditions that lead to more data anomalies.
- Bike Maintenance: Classic bikes might require more maintenance or might be more prone to issues that could reflect as outliers in the data.

- Insight: Docked bikes have the highest mean ride duration, suggesting that they are associated with longer trips compared to the other bike types.
- Possible Reasons: This could indicate that docked bikes are used for longer journeys, possibly for commuting or travel between locations that are not easily reachable by shorter rides. It might also be indicative of users keeping docked bikes for extended periods.
This analysis suggests that electric bikes tend to be used for shorter, more consistent trips, while classic and docked bikes are associated with longer and more varied ride durations, with classic bikes showing the greatest variability and number of long-duration rides.

Outlier Trends by Time and Day: Weekends: Outliers are more common, with the highest numbers on Saturdays for both casual and member riders. Weekdays: Casual riders have more outliers on Mondays, while member riders see more on Tuesdays and Wednesdays. Time of Day: The afternoon sees the highest number of outliers for both casual and member riders, followed by night for casual riders and morning for members.

Seasonal Patterns: Casual riders show a peak in outlier rides during the warmer months (May to September), with the highest in July. Members have a stable ride pattern throughout the year with minor peaks in the warmer months.

The analysis reveals that casual riders are responsible for the majority of outliers, particularly during the afternoon and on weekends. Classic bikes are associated with the highest number of outliers, indicating potential usage or maintenance issues. Outliers are more frequent during the warmer months, reflecting higher overall ride activity.

### Recommendations
- Targeted Maintenance: Focus on improving the maintenance of classic bikes to reduce the number of outliers.
- Enhanced Monitoring: Increase monitoring during peak times (afternoon) and on weekends to identify and address issues promptly.
- User Engagement: Educate casual riders about proper bike usage to minimize long-duration outliers.
- Seasonal Adjustments: Prepare for higher outlier rates during warmer months by ensuring adequate resources and support are available.
- Station-Specific Strategies: Implement strategies at high-outlier stations like Streeter Dr & Grand Ave to manage and reduce outlier occurrences. By addressing these areas, we can improve data quality, enhance user experience, and optimize operational efficiency for the bike-sharing service.