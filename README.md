Data Analytics Projects

Project 1 Exploratory Data Analysis

Project Description: Exploratory Data Analysis (EDA) on the City of Vancouver Greenest City Projects Dataset 

Project Title: City of Vancouver greenest city project: An Exploratory Data Analysis

Objective:
The objective of this project is to determine whether a correlation exists between the number of projects in CATEGORY2 and the Geo Local Areas where they are implemented. This insight is vital for understanding the geographic distribution of green building projects and identifying patterns or clustering within urban areas. By leveraging data from the City of Vancouver Greenest City Projects dataset, this analysis aims to support sustainable city development and environmental preservation efforts.

Dataset: The dataset contains information about projects under the City of Vancouver's Greenest City Action Plan, aimed at advancing sustainability and environmental preservation. It includes 324 entries with the following columns:

•	MAPID: A unique identifier assigned to each project.

•	NAME: The name of the project, representing its official title.

•	CATEGORY1: Primary classification of the project (e.g., "City projects," "Private projects").

•	CATEGORY2: Secondary classification of the project, such as "Climate-Leadership" or "Green-Buildings."

•	ADDRESS: The physical address of the project, if available.

•	SHORT_DESCRIPTION: A brief description summarizing the project's objectives or impact.

•	URL, URL2, URL3: Links to additional resources or pages about the project for further information.

•	Geo Local Area: The geographic region within Vancouver where the project is located, such as Mount Pleasant or other neighborhoods.

Draw io Diagram Data Analytic Platform (City of Vancouver – Domain- Greenest city projects)

![image](https://github.com/user-attachments/assets/5b876584-1bf0-42c8-b246-0019b1aa4b62)
 
Exploratory Analysis Question

Is there a correlation between the number of projects in CATEGORY2 and the Geo Local Areas they are located in? 

The objective of this project is to determine whether a correlation exists between the number of projects in CATEGORY2 and the Geo Local Areas where they are implemented. 

Methodology:

Data Ingestion

Objective: Upload and organize raw greenest city projects data into AWS S3 for easy access and processing.

Steps:

1.	Created S3 buckets (raw-data-nisha) to store the raw Excel data files.

2.	Structured the data with subfolders by quarter (ingestion_quarter=4) to accommodate updates and frequent access requirements.

3.	Configured storage class as S3 Standard to ensure high performance for analytics.

Data Profiling Objective: Assess data quality, identify missing values, and gather descriptive statistics. 

Steps:

1.	Created new buckets to store profiling results (trf-data-nisha).

2.	Connected the dataset to AWS Glue DataBrew for profiling.

3.	Ran profiling jobs to analyze data quality and missing values for each column.

4.	Stored profiling results in designated subfolders.

Data Cleaning Objective: Standardize and prepare data for transformation by addressing inconsistencies and missing information. 

Steps:

1.	Created a new project in AWS Glue DataBrew for cleaning.

2.	Applied recipes to rename and standardize column names.

3.	Addressed null values and optimized dataset size using compression (Snappy format).

4.	Saved cleaned data in dedicated system and user subfolders in S3.

Data Pipeline Design Objective: Transform and aggregate data to find out correlation 

Steps:

1.	Used AWS Glue Visual ETL for data transformation.

2.	Extracted data from Amazon S3 for initial exploration and mapping.

3.	Filtered out unnecessary columns to clean up data.

4.	Renamed keys for the join operation to ensure smooth merging of datasets.

5.	Joined datasets based on specified keys for comparison and transformation.

6.	Applied derived column transformations to enhance data insights.

7.	Performed additional processing steps for validation.

8.	Loaded the final output into S3 for further analysis.

Data Analysis Objective: To determine whether a correlation exists between the number of projects in CATEGORY2 and the Geo Local Areas where they are implemented. 

Steps:

1.	Queried aggregated results in S3 using analytics tools.

2.	Examined the Measured the correlation between the number of CATEGORY2 projects and their Geo Local Areas

3.	Assessed the dispersion of green-building initiatives across Vancouver.

Tools and Technologies

The following tools and technologies were utilized to perform the analysis of correlation, ensuring efficient data management, processing, and analytics:

AWS Services - The Data Analytics Platform (DAP) leveraged several AWS components for scalable and robust data processing:

•	Amazon S3

•	AWS Glue DataBrew

•	AWS Glue

Insights and Findings

From the analysis , the following insights and findings were observed:

•	Identified patterns, such as clustering of CATEGORY2 projects in specific Geo Local Areas.

•	Determined that certain regions show stronger positive correlations, indicating a higher density of green-building initiatives.

•	Highlighted underrepresented areas for potential development focus.

