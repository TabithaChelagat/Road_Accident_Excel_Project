**PROJECT SUMMARY: Analyzing UK Road Accident Data (2021-2022)**

***Objective:***

The objective of this project is to analyze road accident data from the UK Transport Department spanning the period from 2021 to 2022. The aim is to gain insights into the trends, patterns, and factors contributing to road accidents during this time frame. Additionally, the project seeks to develop an interactive dashboard to visualize key findings and facilitate data-driven decision-making by stakeholders.

***Methodology:***

- *Data Collection:* Road accident data for the specified period will be obtained from the UK Transport Department's database or relevant sources.

- *Data Cleaning and Preparation:* The collected data will undergo thorough cleaning and preprocessing to handle missing values, outliers, and inconsistencies. Data preparation steps 
   will include standardizing formats, encoding categorical variables, and aggregating data as necessary.

- *Exploratory Data Analysis (EDA):* EDA techniques will be employed to explore the dataset and uncover meaningful insights. This will involve statistical analysis, time series 
   analysis, and visualization to identify trends, correlations, and factors influencing road accidents.

- *Dashboard Development:* Using Excel for visualization, an interactive dashboard will be designed to present key findings from the analysis. The dashboard will provide user-friendly 
   access to insights and allow for dynamic exploration of the data.

***Deliverables:***

- Comprehensive analysis report summarizing key findings, trends, and recommendations based on the road accident data.

- Interactive dashboard showcasing visualizations of accident trends, geographical hotspots, contributing factors, and demographic analysis.

- Presentation of findings and dashboard demonstration to stakeholders within the UK Transport Department.

***Expected Impact:***

The analysis and dashboard developed through this project will provide valuable insights to the UK Transport Department for informed decision-making and policy formulation aimed at improving road safety. By identifying high-risk areas, contributing factors, and demographic patterns associated with road accidents, targeted interventions can be implemented to reduce accident rates and enhance overall road safety measures.


**QUESTIONS TO ANSWER**

- Primary KPI: Total casualties that happened after the accident.

- Primary KPI's: Total casualties and their percentage concerning accident severity and maximum casualties by type of vehicle.

- Secondary KPI's:
  
   -Total casualties concerning vehicle type.
  
   -Monthly trend showing comparison of casualties in the current and previous year.
  
   -Maximum casualties by road type.
  
   -Distribution of total casualties by road surface.
  
   -Relation between casualties by Area/Lighting conditions and Location.


**DATA SOURCE**

Link to the dataset that will be used for our analysis, https://docs.google.com/spreadsheets/d/1R_uaoZL18nRbqC_MULVne90h3SdRbAyn/edit?usp=sharing&ouid=116890999875311477003&rtpof=true&sd=true.


**DATA EXPLORATION**


With a total of 307,874 data entries and zero nulls and duplicates, our dataset has 20 columns as shown below:


| Column Name              | Description                   |
|--------------------------|-------------------------------|
| Accident_Index           | Unique identifier for the accident |
| Accident Date            | Date of the accident          |
| Day_of_Week              | Day of the week of the accident |
| Junction_Control         | Type of junction control      |
| Junction_Detail          | Detail of junction            |
| Accident_Severity        | Severity of the accident      |
| Latitude                 | Latitude of the accident location |
| Light_Conditions         | Light conditions at the time of the accident |
| Local_Authority_(District) | Local authority district      |
| Carriageway_Hazards      | Hazards present on the carriageway |
| Longitude                | Longitude of the accident location |
| Number_of_Casualties     | Number of casualties involved in the accident |
| Number_of_Vehicles       | Number of vehicles involved in the accident |
| Police_Force             | Police force reporting the accident |
| Road_Surface_Conditions  | Road surface conditions at the time of the accident |
| Road_Type                | Type of road                  |
| Speed_limit              | Speed limit of the road where the accident occurred |
| Time                     | Time of the accident          |
| Urban_or_Rural_Area      | Urban or rural area           |
| Weather_Conditions       | Weather conditions at the time of the accident |
| Vehicle_Type             | Type of vehicle involved in the accident |


**DATA CLEANING**

Using the Find and Replace Excel function 

``(Ctrl + H)``

, we successfully corrected the spelling errors in the Accident_Severity column. Specifically, the 49 data
entries that were misspelled as "Fetal" were found and replaced with the correct spelling "Fatal". This ensures the accuracy and integrity of the data in the dataset.


**DATA FORMATTING**

***Extracting month from Accident Date column:***

Using the following function,

``=TEXT(B3,"mmm")``

, the month was extracted from the Accident Date column. This Excel function, ``TEXT``, allows formatting of cell contents based on a specified format code. In this case, ``B3`` represents the cell containing the date, and ``"mmm"`` is the format code that extracts the abbreviated month name from the date in cell ``B3``. This process enables us to isolate and analyze the months in which accidents occurred, providing valuable insights into temporal patterns and trends.

***Extracting year from Accident Date column:***

Using the Excel function,

``=TEXT(B3,"yyyy")``

, we extracted the year from the Accident Date column. This function converts the date in cell B3 into a text format displaying only the year portion.


***DATA ANALYSIS***

We did the following analyses to provide insights into the questions to be answered.

All our analyses will be conducted using pivot tables.

1. ***Total casualties that occurred following the accident***. 

|        Number_of_Casualties |
|-----------------------------|
|            417883           |


The sum of ``417,883`` casualties represents the total number of casualties that occurred between the years 2021 and 2022.


2. ***Total casualties and their percentage concerning accident severity***.


| Severity   | Sum of Number_of_Casualties |
|------------|-----------------------------|
| Fatal      | 7135 (1.7%)                 |
| Serious    | 59312 (14.2%)               |
| Slight     | 351436 (84.1%)              |
| Grand Total| 417883                      |

*Summary of findings:*

The provided data presents a breakdown of total casualties categorized by accident severity between the years 2021 and 2022. Here's a summary:

- *Fatal Casualties:* There were ``7,135`` fatal casualties, accounting for approximately ``1.7%`` of the total casualties.
  
![UK Road Accident Dashboard (1)](https://github.com/tabby1307/Road_Accident_Excel_Project/assets/112205355/4e98d550-7b79-440e-9e53-85aa291fd814)

- *Serious Casualties:* The number of serious casualties was ``59,312``, constituting approximately ``14.2%`` of the total casualties.

![Screenshot (188) (1)](https://github.com/tabby1307/Road_Accident_Excel_Project/assets/112205355/8055af1f-c9ec-43e7-b15a-cd9b2cf1797f)

- *Slight Casualties:* The majority of casualties were categorized as slight, with a total of ``351,436`` casualties, representing about ``84.1%`` of the total.

![Screenshot (188) (2)](https://github.com/tabby1307/Road_Accident_Excel_Project/assets/112205355/4b2ad1c1-3832-436e-a274-83fa7058d56f)


In summary, the data illustrates that while fatal and serious casualties make up a smaller proportion of the total, slight casualties constitute the majority of the incidents, 
highlighting the importance of addressing factors contributing to minor accidents to improve overall road safety.


3. ***Number of casualties categorized by vehicle type between the years 2021 and 2022***. 


| Type of vehicle     | Sum of Number_of_Casualties |
|---------------------|------------------------------|
| Agricultural vehicle| 1032                         |
| Cars                | 333485                       |
| Bus                 | 12798                        |
| Van                 | 33472                        |
| Bike                | 33672                        |
| Others              | 3424                         |
| Grand Total         | 417883                       |

*Summary of findings:*

- *Agricultural Vehicle:* There were ``1,032`` casualties involving agricultural vehicles.

- *Cars:* The highest number of casualties occurred in incidents involving cars, totaling ``333,485`` casualties.

- *Bus:* There were ``12,798`` casualties involving buses.

- *Van:* The number of casualties involving vans was ``33,472``.

- *Bike:* There were ``33,672`` casualties involving bicycles.

- *Others:* Casualties involving other types of vehicles totaled ``3,424``.

![UK Road Accident Dashboard (5)](https://github.com/tabby1307/Road_Accident_Excel_Project/assets/112205355/4622873f-d05b-4ea5-a5e1-461eef4a39a4)

  
The data indicates that incidents involving cars resulted in the highest number of casualties. Therefore, we will focus our analysis on casualties involving cars to gain deeper insights into the factors contributing to these incidents.

![UK Road Accident Dashboard (2)](https://github.com/tabby1307/Road_Accident_Excel_Project/assets/112205355/a965ceef-9ed2-4ba4-add2-cd6ca05ad6a5)


Approximately ``80%`` of the total casualties involved cars. This highlights the significant impact of car-related accidents and underscores the importance of understanding and addressing factors contributing to these incidents to improve overall road safety.


4. ***Monthly trend showing the comparison of casualties in the current and previous year***.

| Month | 2021 Casualties | 2022 Casualties |
|-------|------------------|------------------|
| Jan   | 18173            | 13163            |
| Feb   | 14648            | 14804            |
| Mar   | 17815            | 16575            |
| Apr   | 17335            | 15767            |
| May   | 18852            | 16775            |
| Jun   | 18728            | 17230            |
| Jul   | 19682            | 17201            |
| Aug   | 18797            | 16796            |
| Sep   | 18456            | 17500            |
| Oct   | 20109            | 18287            |
| Nov   | 20975            | 18439            |
| Dec   | 18576            | 13200            |


*Summary of the trends observed:*

- Overall Trend: In general, there appears to be a fluctuating trend in casualties between the two years, with some months experiencing increases while others see decreases.

![Screenshot (188) (3)](https://github.com/tabby1307/Road_Accident_Excel_Project/assets/112205355/3da6f935-102f-4eeb-a1b5-7d88b4922f4c)


Monthly Comparison:

- *January to March:* The casualties in 2021 started higher compared to 2022, but by March, the numbers started to converge, with 2022 casualties slightly lower.

- *April to June:* From April to June, casualties in 2022 were consistently lower compared to the previous year, indicating a potential decrease in accidents during these months.

- *July to September:* In July and August, casualties in 2022 remained slightly lower than in 2021, but by September, they started to rise again, surpassing the previous year's numbers.

- *October to December:* From October to December, casualties in 2022 consistently exceeded those in 2021, with the largest difference observed in November and December.

- *Seasonal Variations:* There appears to be seasonal variation in casualty rates, with casualties generally increasing during the warmer months and decreasing during the colder months.


5. ***Maximum casualties by road type***

The provided data illustrates the maximum casualties categorized by road type

| Road Type           | Sum of Number_of_Casualties |
|---------------------|------------------------------|
| (blank)             | 1.9k                         |
| Slip road           | 4.7k                         |
| One way street      | 7.4k                         |
| Roundabout          | 26.8k                        |
| Dual carriageway    | 67.4k                        |
| Single carriageway  | 309.7k                       |
| Grand Total         | 417.9k                       |


*Summary of the findings:*

- *Single Carriageway:* Single carriageways recorded the highest number of casualties, totaling ``309.7k``, which accounts for approximately ``74.2%`` of the grand total. This suggests that accidents on single-carriageways contribute significantly to overall casualties.

- *Dual Carriageway:* Dual carriageways had the second-highest number of casualties, with a total of ``67.4k``, making up about ``16.1%`` of the grand total. While this is substantially lower than single carriageways, it still represents a significant proportion of casualties.

- *Roundabout:* Roundabouts witnessed a considerable number of casualties, totaling ``26.8k``, comprising approximately ``6.4%`` of the grand total. This highlights the importance of road safety measures at roundabouts to mitigate accidents.

- *One-Way Street and Slip Road:* One-way streets and slip roads recorded relatively lower numbers of casualties compared to single and dual carriageways, with ``7.4k`` and ``4.7k`` casualties respectively. However, they still contribute to the overall casualty count.

![UK Road Accident Dashboard (3)](https://github.com/tabby1307/Road_Accident_Excel_Project/assets/112205355/864f09ea-faa2-4cf0-afc3-76bf72937496)


These findings underscore the importance of implementing targeted safety measures, such as improved signage, traffic management, and speed enforcement, particularly on single and dual carriageways, to reduce the incidence of accidents and enhance road safety. Additionally, addressing safety concerns at roundabouts can also help in mitigating casualties at these locations.


6. ***Maximum casualties by road surface***

The data revealed the following,


| Road Surface   | Number of Casualties |
|----------------|----------------------|
| Dry            | 279445               |
| (blank)        | 396                  |
| Wet            | 115261               |
| Snow or Ice    | 22781                |

*Summary of findings:*

- *Dry Surface:* The majority of casualties occurred on dry road surfaces, with a total of ``279,445`` casualties. Dry road conditions accounted for the highest number of casualties, 
   indicating that most accidents occurred when road surfaces were dry.

- *Wet Surface:* Wet road surfaces accounted for a significant number of casualties, totaling ``115,261``. This suggests that rainy or wet conditions contribute to a considerable portion of 
   accidents, although the number is lower than casualties on dry surfaces.

- *Snow or Ice:* Despite being less common, accidents on snow or ice-covered road surfaces still resulted in a notable number of casualties, totaling ``22,781``. This underscores the 
   increased risk associated with driving in adverse weather conditions such as snow or ice.

- *Unknown Surface:* A small number of casualties ,``396``, were reported with an unknown road surface type, which could be due to data recording or reporting inconsistencies.

![UK Road Accident Dashboard (4)](https://github.com/tabby1307/Road_Accident_Excel_Project/assets/112205355/02fb6d36-4bbd-49ba-9fa2-6c20d9705033)


Overall, the data highlights the impact of road surface conditions on road safety, with dry surfaces being the most common setting for accidents, followed by wet surfaces. Adverse weather conditions like snow or ice also pose significant risks to road users, emphasizing the importance of exercising caution and implementing appropriate safety measures during inclement weather.


7. ***Relation between casualties by location and lighting conditions***.

*Location:*

| Location | Sum of Number_of_Casualties |
|----------|-----------------------------|
| Rural    |           162.0k            |
| Urban    |           255.9k            |
| Total    |           417.9k            |


*Summary of findings:*

- *Urban Casualties:* There were a total of ``255.9k`` casualties reported in urban areas, representing approximately ``61.3%`` of the total. This indicates a higher concentration of 
   accidents in urban environments.

- *Rural Casualties:* Casualties reported in rural areas amounted to ``162.0k``, accounting for around ``38.7%`` of the total. Although lower than urban casualties, accidents in rural settings 
   still contribute significantly to the overall casualty count.

![UK Road Accident Dashboard (6)](https://github.com/tabby1307/Road_Accident_Excel_Project/assets/112205355/f398c434-d26b-4e30-b595-37482d4ef305)


The data suggests a higher incidence of accidents in urban areas compared to rural areas, highlighting the need for targeted road safety measures and infrastructure improvements in urban environments to reduce the risk of accidents and enhance overall road safety.


*Lighting conditions:*


| Lighting Conditions | Sum of Number_of_Casualties |
|---------------------|-----------------------------|
| Daylight            |           304,963           |
| Dark                |           112,920           |
| Total               |           417,883           |


*Summary of findings:*

- *Daylight Casualties:* The majority of casualties, totaling ``304,963``, occurred in daylight conditions. This indicates that the majority of accidents happen when visibility is optimal, possibly due to higher traffic volume during the day.

- *Dark Casualties:* Casualties reported in dark conditions amounted to ``112,920``. Although significantly lower than daylight casualties, accidents in dark conditions still contribute substantially to the overall casualty count.

![Screenshot (188) (4)](https://github.com/tabby1307/Road_Accident_Excel_Project/assets/112205355/c8b30268-18a0-494d-939f-59010e132291)


The data suggests that accidents are more prevalent during daylight hours compared to dark conditions. However, it's essential to implement appropriate safety measures, such as improved street lighting and driver awareness campaigns, to mitigate the risk of accidents in both daylight and dark conditions.


**DASHBOARD**

![Screenshot (188)](https://github.com/tabby1307/Road_Accident_Excel_Project/assets/112205355/88fb8652-b08a-4536-9fad-ff4603680dc5)


The dashboard features a user-friendly filter panel comprising a timeline for navigating through different months and a slicer for location (urban/rural), empowering stakeholders to explore the data efficiently.

Positioned on the left side of the dashboard are five icons, each serving a distinct purpose. 

- Clicking on the second icon directs users to the dashboard sheet within our Excel file, providing access to the raw data.
  
- The third icon leads to the data analysis sheet, housing comprehensive analyses conducted on the dataset.
  
- Utilizing the fourth icon facilitates emailing the dashboard directly to stakeholders.
 
- Lastly, clicking on the last icon redirects users to the UK Road Accident website, facilitating access to additional information and resources pertinent to road safety.



**CONCLUSION**


- ***Trend Analysis:*** The data analysis reveals various trends and patterns regarding road accidents between 2021 and 2022. Casualties varied by month, with fluctuations observed across different road types, lighting conditions, and urban/rural areas.

- ***Contributing Factors:*** Factors such as road surface conditions, weather conditions, and lighting play a significant role in accident occurrence. Single carriageways and urban areas reported higher casualties, while daylight conditions accounted for the majority of accidents.

- ***Key Findings:*** Urban areas experienced a higher concentration of accidents compared to rural areas. Additionally, accidents were more prevalent in daylight conditions, highlighting the need for improved safety measures during optimal visibility.


**Actions to be Taken:**

- ***Targeted Safety Campaigns:*** Implement targeted safety campaigns to raise awareness among drivers, cyclists, and pedestrians about road safety practices, particularly in urban areas with high accident rates.

- ***Infrastructure Improvements:*** Enhance infrastructure in accident-prone areas, such as roundabouts and single carriageways, to improve traffic flow and reduce the risk of collisions.

- ***Weather-Responsive Measures:*** Implement weather-responsive measures, such as road surface treatment and increased monitoring during adverse weather conditions like rain, snow, or ice, to mitigate accidents.

- ***Enhanced Lighting:*** Improve street lighting in areas with high accident rates, especially during nighttime, to enhance visibility and reduce the risk of accidents in dark conditions.

- ***Data-Driven Interventions:*** Continuously monitor and analyze accident data to identify emerging trends and hotspots, enabling proactive interventions and targeted safety measures.

- ***Collaboration:*** Foster collaboration between government agencies, law enforcement, and community stakeholders to develop comprehensive road safety strategies and initiatives.


By implementing these actions, we can work towards reducing the incidence of road accidents, minimizing casualties, and creating safer road environments for all road users.















