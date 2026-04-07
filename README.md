 Overview
This project delivers a comprehensive Tableau dashboard built on a globally sourced Data Science salary dataset (DS.csv). The dashboard brings together 7 coordinated visualizations on a single screen, enabling users to:



 Problem Statement
The data science job market is fast-growing and globally distributed, but compensation benchmarks are scattered and hard to compare. Professionals and hiring managers face key unanswered questions:

How much does experience level (Entry → Senior → Expert) impact data science salaries?
Do full-time, contract, part-time, and freelance roles pay differently?
Which specific job titles (e.g., ML Engineer vs. Data Analyst vs. Research Scientist) command the highest salaries?
How does geography affect pay — which countries lead in data science compensation?
Are larger companies actually paying more than small ones?
Where do most data science professionals reside, and does it match where companies are headquartered?

This dashboard consolidates all of these questions into a single, filterable view — turning a raw CSV into actionable compensation intelligence.

 Dataset




 Tools & Technologie
Tool / TechnologyPurposeTableau Desktop 2025.1Dashboard development and all visualizationsTableau PublicPublishing and sharing the dashboard onlineCSV (DS.csv)Raw data sourceTableau Hyper ExtractIn-memory data extract for fast query performanceCalculated FieldsCustom layout and aggregation metricsGeographic RolesCountry-level geocoding for the choropleth mapField AliasesHuman-readable labels for coded fields (e.g., SE → Senior)

⚙️ Methods

Data Connection — Connected Tableau Desktop to DS.csv using a Text File connection with UTF-8 encoding and comma delimiter.
Data Extraction — Built a Tableau Hyper extract (.hyper) for optimized in-memory query performance across all 7 worksheets.
Field Aliasing — Applied human-readable aliases to all coded fields so dashboards display clearly without data transformation:

Experience Level: EN → Entry Level, MI → Intermediate, SE → Senior, EX → Expert
Employment Type: FT → Full Time, PT → Part Time, CT → Contract, FL → Freelance
Company Size: S → Small, M → Medium, L → Large


Geocoding — Assigned Company Location the semantic geographic role [Country].[Name], enabling Tableau to auto-generate latitude/longitude for the world map.
Visualization Design — Built 7 individual worksheets, each targeting a specific analytical question, then assembled into a unified dashboard layout.
Color Encoding — Applied the sf_default palette for categorical dimension breakdowns and a sequential blue palette for the salary-gradient map.
Dashboard Assembly — Arranged all 7 views in a horizontal/vertical tiled zone layout on Dashboard 1, optimized for a full-screen, single-scroll experience.


💡 Key Insights
💰 1. Average Salary by Experience Level & Employment Type
(Shape Chart — Employment Type × Experience Level vs. Avg Salary in USD)

Expert-level professionals command the highest average salaries across every employment type.
Full-time roles consistently pay more than Contract, Part-Time, or Freelance equivalents at every experience tier.
The steepest salary jump occurs between Intermediate and Senior, indicating mid-career progression is the most financially rewarding transition.
Contract roles at Expert level can approach full-time salaries, reflecting the premium commanded by specialized independent contractors.

🔠 2. Average Salary by Job Title & Experience Level
(Highlight Table — Job Title × Experience Level, colored by Avg Salary in USD)

Machine Learning Engineers, Staff Data Scientists, and AI Research roles appear among the highest-compensated titles.
At Expert level, niche roles such as 3D Computer Vision Researcher rank at the very top of the pay scale.
ETL Developers and Finance Data Analysts sit at the lower end of the salary range, even at Senior level.
The ~50 job titles reveal how fragmented and specialized the data science field has become — from NLP Specialists to MLOps Engineers to Business Intelligence Analysts.

🥧 3. Employment Type Distribution
(Pie Chart — Employment Type split by count)

Full-time employment dominates the dataset by a wide margin, reflecting the industry norm for data science roles.
Contract, Part-Time, and Freelance positions together represent a small fraction, confirming that data science is predominantly a salaried profession rather than a gig economy role.

🥧 4. Experience Level Distribution
(Pie Chart — Experience Level split by count)

Senior-level professionals form the largest share of the dataset, suggesting the survey skews toward mid-to-late career practitioners.
Entry Level has a meaningful presence, consistent with rapid market growth attracting new entrants.
Expert-level roles are the rarest segment — underscoring their scarcity and premium compensation.

🗺️ 5. Map: Average Salary by Country
(Choropleth Map — Company Location colored by Avg Salary in USD)

The United States stands out with the highest average salaries, significantly ahead of all other countries.
Canada, UK, Germany, and Australia form the next tier of high-compensation geographies.
Emerging markets in Asia and Eastern Europe show considerably lower USD-equivalent salaries — partly reflecting local purchasing power and cost-of-living differences.
The map supports drill-down by Job Title filter, allowing comparison of specific role salaries across countries.

📊 6. Top 10 Employee Residence Countries
(Horizontal Bar Chart — Employee Residence by count)

The United States is by far the most represented country of residence, accounting for the majority of all records.
India, United Kingdom, Canada, and Germany follow as the next most common employee residence countries.
The top 10 countries collectively represent the vast majority of the dataset, indicating strong geographic concentration of the global data science talent pipeline.

🥧 7. Total Companies by Size and Location
(Pie Chart — Company Size distribution, filterable by Company Location)

Medium-sized companies hire the most data science professionals, suggesting they represent the primary market for data science talent.
Large enterprises follow in hiring volume; Small companies are the least represented.
When filtered by country, the distribution shifts noticeably — US companies skew toward Medium and Large, while many other countries show a higher proportion of Small companies hiring data science talent.


📸 Dashboard Preview

Dashboard 1 — All 7 charts in a single unified layout:

#WorksheetChart TypeKey Dimensions / Measures1Avg Salary by Experience Level & Employment TypeShape ChartEmployment Type, Experience Level, Avg(Salary in USD)2Avg Salary by Job Title and Experience LevelHighlight TableJob Title, Experience Level, Avg(Salary in USD)3Employee TypePie ChartEmployment Type, Count4Experience LevelPie ChartExperience Level, Count5Map: Average Salary by CountryChoropleth MapCompany Location (geo), Avg(Salary in USD)6Top 10 Employee ResidenceHorizontal BarEmployee Residence, Count7Total Companies by Size and LocationPie ChartCompany Size, Company Location
Open Data_science_dashboard.twbx in Tableau to interact with the live version.

# Tableu---Data-science-job-salary-analysis-
