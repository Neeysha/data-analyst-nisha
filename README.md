Data Analytics Projects
Project 1: Exploratory Data Analysis
Project Description
Title: City of Vancouver Greenest city projects: An Exploratory Data Analysis

Objective: 
To determine whether a correlation exists between the number of projects in CATEGORY2 and the Geo Local Areas where they are implemented.

Dataset
The dataset contains information about projects under the City of Vancouver's Greenest City Action Plan, aimed at advancing sustainability and environmental preservation. It includes 324 entries with the following columns:

• MAPID: A unique identifier assigned to each project.
• NAME: The name of the project, representing its official title.
• CATEGORY1: Primary classification of the project. 
• CATEGORY2: Secondary classification of the project.
• ADDRESS: The physical address of the project, if available.
• SHORT_DESCRIPTION: A brief description summarizing the project's objectives or impact.
• URL, URL2, URL3: Links to additional resources or pages about the project for further information.
• Geo Local Area: The geographic region within Vancouver where the project is located, such as Mount Pleasant or other neighborhoods.

Exploratory Analysis Question
Is there a correlation between the number of projects in CATEGORY2 and the Geo Local Areas they are located in?

Methodology
Data Ingestion:

Uploaded raw data into AWS S3 buckets structured by quarter.
Configured S3 storage class for performance and frequent access.
Data Profiling:

Used AWS Glue DataBrew to analyze data quality and identify missing values.
Stored profiling results in designated subfolders.
Data Cleaning:

Standardized column names and addressed null values.
Compressed data for optimized storage.
Data Pipeline Design:

Filtered and Joined datasets based on specified keys for comparison and transformation.
Applied derived column transformations to enhance data insights.
Data Analysis:

Queried aggregated results in S3 using analytics tools.
Examined the Measured the correlation between the number of CATEGORY2 projects and their Geo Local Areas.
Tools and Technologies
AWS S3: Data storage and organization.
AWS Glue DataBrew: Data profiling and cleaning.
AWS Glue: Visual ETL for data transformation.
Insights and Findings
Identified patterns, such as clustering of CATEGORY2 projects in specific Geo Local Areas.
Determined that certain regions show stronger positive correlations, indicating a higher density of green-building initiatives.
Highlighted underrepresented areas for potential development focus.
Design Draw io Diagram Data Analytic Platform (City of Vancouver – Domain- Greenest City Projects)

![image](https://github.com/user-attachments/assets/5b876584-1bf0-42c8-b246-0019b1aa4b62)

Project 2: Descriptive Analysis
Project Description
Title: City of Vancouver Greenest City Projects: A Descriptive Data Analysis
Objective
To evaluate the contribution of "Green-Buildings" projects within CATEGORY2.

Dataset
The dataset contains information about projects under the City of Vancouver's Greenest City Action Plan, aimed at advancing sustainability and environmental preservation. It includes 324 entries with the following columns:
• MAPID: A unique identifier assigned to each project.
• NAME: The name of the project, representing its official title.
• CATEGORY1: Primary classification of the project. 
• CATEGORY2: Secondary classification of the project.
• ADDRESS: The physical address of the project, if available.
• SHORT_DESCRIPTION: A brief description summarizing the project's objectives or impact.
• URL, URL2, URL3: Links to additional resources or pages about the project for further information.
• Geo Local Area: The geographic region within Vancouver where the project is located, such as Mount Pleasant or other neighborhoods
Descriptive Analysis Question
What percentage of "Green-Buildings" projects are in CATEGORY2?
Methodology
Data Ingestion:

Uploaded raw data into AWS S3 and organized with lifecycle rules for cost optimization.
Data Profiling:

Analyzed data quality and missing values using AWS Glue DataBrew.
Data Cleaning:

Standardized columns and filled missing values.
Saved cleaned data in CSV and Parquet formats for efficient storage.
Data Pipeline Design:

Filtered out unnecessary columns to clean up data.
Aggregated the number of "Green-Buildings" in CATEGORY2.
Saved final results to S3 for further analysis
Tools and Technologies
AWS S3: Data storage and lifecycle management.
AWS Glue DataBrew: Data profiling and cleaning.
AWS Glue ETL: Visual ETL for data transformation and aggregation.
Insights and Findings
46% of CATEGORY2 projects were identified as "Green-Buildings."
This indicates significant representation but also highlights potential for further promotion and development
Impact on Green Initiatives:
"Green-Buildings" are a substantial component of Vancouver's sustainability efforts.
Encouraging greater investment in this category could enhance the city’s green goals.

Conclusion
This descriptive analysis provides a detailed understanding of the important role of "Green-Buildings" in CATEGORY2 projects, supporting Vancouver’s green initiatives and guiding future efforts toward sustainability.

Design Draw io Diagram Data Analytic Platform (City of Vancouver – Domain- Greenest city projects)

![image](https://github.com/user-attachments/assets/5b876584-1bf0-42c8-b246-0019b1aa4b62)

Project 3: Diagnostic Analysis
Project Description
Diagnostic Analysis of Allegations List at UCW Academic Office

Project Title
Investigating Data Quality, Completeness, and Structure of UCW Scholar Allegations list Dataset

Objective
The primary goal is to identify any anomalies, missing data, inconsistencies, or patterns in the dataset that may impact its usability for:

Allegations list
Visualization
Predictive modeling
Insights from this analysis will inform necessary data cleaning and transformation steps, ensuring the dataset's readiness for downstream tasks.
Dataset Overview
The dataset comprises details about scholarly activities conducted by faculty at UCW.

Dataset Fields:
Student_ID: Unique ID of the student involved in the allegation.
Date: Date when the allegation was reported.
Type_of_Violation: Type of academic violation (e.g., Cheating on Exam, Unauthorized Collaboration).
Course_Code: Code of the course in which the violation occurred.
Instructor: Name of the instructor associated with the course.
Severity: Severity level of the allegation (e.g., Severe, Moderate, Minor).
Penalty: Penalty imposed for the violation (e.g., Course Failure, Suspension).
Reported_By: Individual or entity who reported the violation (e.g., Peer, Instructor, TA).
Resolution_Date: Date when the allegation was resolved.
Resolution_Outcome: Final outcome of the resolution process (e.g., Case Closed, Appeal Filed, Under Investigation).
Methodology
Data Collection and Preparation
Data Generation
Simulation Design:

The dataset represents academic integrity allegations reported at UCW.
Simulated data includes real-world attributes such as student IDs, course codes, types of violations, penalties, and resolution outcomes.
Tool Used:

ChatGPT: Generated diverse, consistent, and realistic data entries.
Data Profiling
Conducted using AWS Glue DataBrew to assess data quality, structure, and completeness.

Step 1: Data Ingestion
Uploaded the raw dataset to Amazon S3 (aca-raw-mah).
Connected the dataset to AWS Glue DataBrew for profiling.
Step 2: Profiling Job Setup
Created a profiling job in AWS Glue DataBrew for column-wise analysis.
Included all 10 columns with String Columns (8)and Integer Columns (2)
Step 3: Profiling Insights
Data Quality

Validity: 100% valid values for all columns.
Missing Values: None found (0% missing).
Vaild cells: 400(100%)
Outliers: No outliers detected.
Value Distribution

Distinct Values:
Student_ID: 50 unique values (high cardinality), ensuring consistent identification of each student.
Consistent uniqueness across other fields.
String Length: Uniform distribution for text-based columns.
Other Distinct Values
Type_of_Violation: 5 distinct values (e.g., Cheating on Exam, Plagiarism).
Course_Code: 5 distinct values (e.g., MBA104, MBA103).
Instructor: 5 distinct values (e.g., Dr. Lee, Prof. Brown).
Severity: 3 distinct values (e.g., Minor, Moderate, Severe).
Penalty: 4 distinct values (e.g., Course Failure, Suspension).
Reported_By: 4 distinct values (e.g., Peer, TA, Instructor).
Resolution_Outcome: 4 distinct values (e.g., Case Closed, Appeal Filed).
Step 4: Storage of Results
Stored profiling results in Amazon S3 (Data-Profiling folder in bucket aca-trf-mah).
Step 5: Validation and Action Plan
Validation:

Dataset meets quality standards with no missing values or anomalies.
Data aligns with the expected schema.
Action Plan:

No immediate cleaning required.
Ready for downstream analysis (e.g., transformations, aggregations).
Outcome
The UCW Allegations list dataset is complete, valid, and ready for analysis. The dataset requires no additional cleaning, ensuring a seamless transition to further analytical steps.

Tools and Technologies
AWS Glue DataBrew

Purpose: Automated profiling to assess dataset quality.
Key Features:
Data Quality Metrics: Valid, invalid, and missing values.
Column Profiling: Unique values, distributions, and consistency checks.
Insights Panel: Cardinality, outliers, and top distinct values.
Amazon S3

Purpose: Centralized storage for raw data and profiling results.
Key Features:
Raw Data Storage: Original dataset.
Profiling Results: Stored in the Data-Profiling folder.
Deliverables
Data Profiling Report

Comprehensive report with:
Data Quality Metrics
Column Statistics (value distributions, string lengths)
Schema Validation
Data Quality Insights

All columns validated with 100% valid data and no anomalies.
High cardinality for Faculty_ID ensures unique identification.
Profiling Results Storage

S3 Folder: Data-Profiling within the aca-trf-mah bucket.
Data Visualization

Visual summaries generated by AWS Glue DataBrew:
Bar Charts: Value distributions for key columns.
Top Distinct Values: Most frequent values for each column. Design
Draw io Diagram Data Analytic Platform (Allegations UCW Dataset)

![image](https://github.com/user-attachments/assets/b3c44e92-4c25-4769-8ab3-5b0fece62fb4)

Data Profiling Screen AWS Glue Brew

![image](https://github.com/user-attachments/assets/0b398013-51b7-4d49-b502-b23ef096e689)


