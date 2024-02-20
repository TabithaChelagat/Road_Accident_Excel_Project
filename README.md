Project Summary: Analyzing UK Road Accident Data (2021-2022)

Objective:
The objective of this project is to analyze road accident data from the UK Transport Department spanning the period from 2021 to 2022. The aim is to gain insights into the trends, patterns, and factors contributing to road accidents during this time frame. Additionally, the project seeks to develop an interactive dashboard to visualize key findings and facilitate data-driven decision-making by stakeholders.

Methodology:

Data Collection: Road accident data for the specified period will be obtained from the UK Transport Department's database or relevant sources.

Data Cleaning and Preparation: The collected data will undergo thorough cleaning and preprocessing to handle missing values, outliers, and inconsistencies. Data preparation steps will include standardizing formats, encoding categorical variables, and aggregating data as necessary.

Exploratory Data Analysis (EDA): EDA techniques will be employed to explore the dataset and uncover meaningful insights. This will involve statistical analysis, time series analysis, and visualization to identify trends, correlations, and factors influencing road accidents.

Dashboard Development: Using excel for visualization, an interactive dashboard will be designed to present key findings from the analysis. The dashboard will provide user-friendly access to insights and allow for dynamic exploration of the data.

Deliverables:

Comprehensive analysis report summarizing key findings, trends, and recommendations based on the road accident data.

Interactive dashboard showcasing visualizations of accident trends, geographical hotspots, contributing factors, and demographic analysis.

Presentation of findings and dashboard demonstration to stakeholders within the UK Transport Department.

Expected Impact:
The analysis and dashboard developed through this project will provide valuable insights to the UK Transport Department for informed decision-making and policy formulation aimed at improving road safety. By identifying high-risk areas, contributing factors, and demographic patterns associated with road accidents, targeted interventions can be implemented to reduce accident rates and enhance overall road safety measures.


QUESTIONS TO ANSWER

- Primary KPI: Total casualties that happened after the accident.
- Primary KPIs: Total casualties and their percentage concerning accident severity and maximum casualties by type of vehicle.
- Secondary KPI's:
   -Total casualties concerning vehicle type. 
   -Monthly trend showing comparison of casualties in the current and previous year.
   -Maximum casualties by road type.
   -Distribution of total casualties by road surface.
   -Relation between casualties by Area/Lighting conditions and Location.


DATA SOURCE

Link to dataset that will be used for our analysis, https://docs.google.com/spreadsheets/d/1R_uaoZL18nRbqC_MULVne90h3SdRbAyn/edit?usp=sharing&ouid=116890999875311477003&rtpof=true&sd=true.


DATA EXPLORATION

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


DATA CLEANING

Using the Find and Replace Excel function ``(Ctrl + H)``, we successfully corrected the spelling errors in the Accident_Severity column. Specifically, the 49 data
entries that were misspelled as "Fetal" were found and replaced with the correct spelling "Fatal". This ensures the accuracy and integrity of the data in the dataset.


DATA FORMATTING

Extracting month from Accident Date column:

Using the following function, ``=TEXT(B3,"mmm")``, the month was extracted from the Accident Date column. This Excel function, ``TEXT``, allows formatting of cell contents based on a specified format code. In this case, ``B3`` represents the cell containing the date, and ``"mmm"`` is the format code that extracts the abbreviated month name from the date in cell ``B3``. This process enables us to isolate and analyze the months in which accidents occurred, providing valuable insights into temporal patterns and trends.

Extracting year from Accident Date column:

Using the Excel function ``=TEXT(B3,"yyyy")``, we extracted the year from the Accident Date column. This function converts the date in cell B3 into a text format displaying only the year portion.

DATA ANALYSIS

All our analysis will be conducted using pivot tables.

We initiated our analysis by examining the total casualties that occurred following the accidents. This involved aggregating and summarizing casualty data using pivot tables.

|        Number_of_Casualties |
|-----------------------------|
|            417883           |

The sum of 417,883 casualties represents the total number of casualties that occurred between the years 2021 and 2022.

Next, we analyzed the total casualties and their percentage concerning accident severity.

| Severity   | Sum of Number_of_Casualties |
|------------|-----------------------------|
| Fatal      | 7135 (1.7%)                 |
| Serious    | 59312 (14.2%)               |
| Slight     | 351436 (84.1%)              |
| Grand Total| 417883                      |


The provided data presents a breakdown of total casualties categorized by accident severity between the years 2021 and 2022. Here's a summary:

Fatal Casualties: There were 7,135 fatal casualties, accounting for approximately 1.7% of the total casualties.

Serious Casualties: The number of serious casualties was 59,312, constituting approximately 14.2% of the total casualties.

Slight Casualties: The majority of casualties were categorized as slight, with a total of 351,436 casualties, representing about 84.1% of the total.

In summary, the data illustrates that while fatal and serious casualties make up a smaller proportion of the total, slight casualties constitute the majority of the incidents, 
highlighting the importance of addressing factors contributing to minor accidents to improve overall road safety.

The provided data presents the number of casualties categorized by vehicle type between the years 2021 and 2022. Here's a summary:

| Type of vehicle     | Sum of Number_of_Casualties |
|---------------------|------------------------------|
| Agricultural vehicle| 1032                         |
| Cars                | 333485                       |
| Bus                 | 12798                        |
| Van                 | 33472                        |
| Bike                | 33672                        |
| Others              | 3424                         |
| Grand Total         | 417883                       |


Agricultural Vehicle: There were 1,032 casualties involving agricultural vehicles.

Cars: The highest number of casualties occurred in incidents involving cars, totaling 333,485 casualties.

Bus: There were 12,798 casualties involving buses.

Van: The number of casualties involving vans was 33,472.

Bike: There were 33,672 casualties involving bicycles.

Others: Casualties involving other types of vehicles totaled 3,424.

The data indicates that incidents involving cars resulted in the highest number of casualties. Therefore, we will focus our analysis on casualties involving cars to gain deeper insights into the factors contributing to these incidents.

Approximately 79.7% of the total casualties involved cars. This highlights the significant impact of car-related accidents and underscores the importance of understanding and addressing factors contributing to these incidents to improve overall road safety.





















