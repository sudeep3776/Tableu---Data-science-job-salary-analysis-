 # Project Title 
# Data science job salary analysis 

 # Overview
This project delivers a comprehensive Tableau dashboard built on a globally sourced Data Science salary dataset (DS.csv). The dashboard brings together 7 coordinated visualizations on a single screen, enabling users to:

 # data set used 
 -<a href="https://github.com/sudeep3776/Tableu---Data-science-job-salary-analysis-/blob/main/Data%20science.csv"> Data set view 
 
 -<a href="https://github.com/sudeep3776/Tableu---Data-science-job-salary-analysis-/blob/main/Data%20science%20dashboard.twbx">Dashboard view 
 
 Screenshot <img width="1457" height="882" alt="Screenshot dashboard" src="https://github.com/user-attachments/assets/0aeec72f-8ce7-47f3-ba87-aa1944a01033" />

 # Problem Statement
The data science job market is fast-growing and globally distributed, but compensation benchmarks are scattered and hard to compare. Professionals and hiring managers face key unanswered questions:

How much does experience level (Entry → Senior → Expert) impact data science salaries?
Do full-time, contract, part-time, and freelance roles pay differently?
Which specific job titles (e.g., ML Engineer vs. Data Analyst vs. Research Scientist) command the highest salaries?
How does geography affect pay — which countries lead in data science compensation?
Are larger companies actually paying more than small ones?
Where do most data science professionals reside, and does it match where companies are headquartered?

This dashboard consolidates all of these questions into a single, filterable view — turning a raw CSV into actionable compensation intelligence.


## Tools & Technologies

Tool / TechnologyPurposeTableau Desktop 2025.1Dashboard development and all visualizationsTableau PublicPublishing and sharing the dashboard onlineCSV (DS.csv)Raw data sourceTableau Hyper ExtractIn-memory data extract for fast query performanceCalculated FieldsCustom layout and aggregation metricsGeographic RolesCountry-level geocoding for the choropleth mapField AliasesHuman-readable labels for coded fields (e.g., SE → Senior)

## Methods

###Data Connection — Connected Tableau Desktop to DS.csv using a Text File connection with UTF-8 encoding and comma delimiter.
###Data Extraction — Built a Tableau Hyper extract (.hyper) for optimized in-memory query performance across all 7 worksheets.
###Field Aliasing — Applied human-readable aliases to all coded fields so dashboards display clearly without data transformation:




## Key Insights
 1. Average Salary by Experience Level & Employment Type
(Shape Chart — Employment Type × Experience Level vs. Avg Salary in USD)


 2. Average Salary by Job Title & Experience Level
(Highlight Table — Job Title × Experience Level, colored by Avg Salary in USD)


3. Employment Type Distribution
(Pie Chart — Employment Type split by count)


 4. Experience Level Distribution
(Pie Chart — Experience Level split by count)


5. Map: Average Salary by Country
(Choropleth Map — Company Location colored by Avg Salary in USD)


 6. Top 10 Employee Residence Countries
(Horizontal Bar Chart — Employee Residence by count)


 7. Total Companies by Size and Location
(Pie Chart — Company Size distribution, filterable by Company Location)


## Dashboard Preview

Dashboard 1 — All 7 charts in a single unified layout:

#WorksheetChart TypeKey Dimensions / Measures1Avg Salary by Experience Level & Employment TypeShape ChartEmployment Type, Experience Level, Avg(Salary in USD)2Avg Salary by Job Title and Experience LevelHighlight TableJob Title, Experience Level, Avg(Salary in USD)3Employee TypePie ChartEmployment Type, Count4Experience LevelPie ChartExperience Level, Count5Map: Average Salary by CountryChoropleth MapCompany Location (geo), Avg(Salary in USD)6Top 10 Employee ResidenceHorizontal BarEmployee Residence, Count7Total Companies by Size and LocationPie ChartCompany Size, Company Location


