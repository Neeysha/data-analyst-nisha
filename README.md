# Data Analytics Projects

## Project 1: Exploratory Data Analysis

### Project Description
**Title:** City of Vancouver Greenest city projects: An Exploratory Data Analysis

### **Objective**
To determine whether a correlation exists between the number of projects in CATEGORY2 and the Geo Local Areas where they are implemented.

### **Dataset** 
The dataset contains information about projects under the City of Vancouver's Greenest City Action Plan, aimed at advancing sustainability and environmental preservation. It includes 324 entries with the following columns:
- **MAPID**: A unique identifier assigned to each project.
- **NAME**: The name of the project, representing its official title.CATEGORY1: Primary classification of the project. 
- **CATEGORY2**: Secondary classification of the project.
- **ADDRESS**: The physical address of the project, if available.
- **SHORT_DESCRIPTION**: A brief description summarizing the project's objectives or impact.
- **URL, URL2, URL3**: Links to additional resources or pages about the project for further information.
- **Geo Local Area**: The geographic region within Vancouver where the project is located, such as Mount Pleasant or other neighborhoods.

### **Exploratory Analysis Question**
Is there a correlation between the number of projects in CATEGORY2 and the Geo Local Areas they are located in?

### **Methodology**
1. **Data Ingestion:**
  - Uploaded raw data into AWS S3 buckets structured by quarter.
   - Configured S3 storage class for performance and frequent access.

2. **Data Profiling:**
 - Used AWS Glue DataBrew to analyze the data quality and identify the data errors
 - Stored the output of data profiling results in designated subfolders.

3. **Data Cleaning:**
 - Standardized column names and enhanced data quality vy addressing null and wrong data values.
 - Compressed data for optimized storage.

4. **Data Pipeline Design:**
  - Filtered and transformed data for analysis.
  - Applied derived column transformations to enhance data insights

5. **Data Analysis:**
 - Queried aggregated results and analyzed ticket issuance trends.
 - Examined the Measured the correlation between the number of CATEGORY2 projects and their Geo Local Areas.

### **Tools and Technologies**
- **AWS S3:** Data storage and organization.
- **AWS Glue DataBrew:** Data profiling and cleaning.
- **AWS Glue:** Visual ETL for data transformation.

### **Insights and Findings**
- Identified patterns, such as clustering of CATEGORY2 projects in specific Geo Local Areas.
- Determined that certain regions show stronger positive correlations, indicating a higher density of green-building initiatives.
- Highlighted underrepresented areas for potential development focus.

**Design**
Draw io Diagram Data Analytic Platform (City of Vancouver – Domain- Greenest City Projects)

![image](https://github.com/user-attachments/assets/5b876584-1bf0-42c8-b246-0019b1aa4b62)

---
## **Project 2: Descriptive Analysis**

### **Project Description** 
**Title:** City of Vancouver Greenest City Projects: A Descriptive Data Analysis

### **Objective**
To evaluate the contribution of "Green-Buildings" projects within CATEGORY2.

### **Dataset**
The dataset contains information about projects under the City of Vancouver's Greenest City Action Plan, aimed at advancing sustainability and environmental preservation. It includes 324 entries with the 
following columns:
- **MAPID**: A unique identifier assigned to each project.
- **NAME**: The name of the project, representing its official title.CATEGORY1: Primary classification of the project. 
- **CATEGORY2**: Secondary classification of the project.
- **ADDRESS**: The physical address of the project, if available.
- **SHORT_DESCRIPTION**: A brief description summarizing the project's objectives or impact.
- **URL, URL2, URL3**: Links to additional resources or pages about the project for further information.
- **Geo Local Area**: The geographic region within Vancouver where the project is located, such as Mount Pleasant or other neighborhoods.

### **Descriptive Analysis Question**
What percentage of "Green-Buildings" projects are in CATEGORY2?

### **Methodology**
**Data Ingestion:**
 - Uploaded raw data into AWS S3 and organized with lifecycle rules for cost optimization.

2. **Data Profiling:**
   - Analyzed data quality and missing values using AWS Glue DataBrew.

3. **Data Cleaning:**
   - Standardized columns and filled missing values.
   - Saved cleaned data in CSV and Parquet formats for efficient storage.

4. **Data Pipeline Design:**
  - Filtered out unnecessary columns to clean up data.
  - Aggregated the number of "Green-Buildings" in CATEGORY2.
  - Saved final results to S3 for further analysis

### **Tools and Technologies**
- **AWS S3:** Data storage and lifecycle management.
- **AWS Glue DataBrew:** Data profiling and cleaning.
- **AWS Glue ETL:** Visual ETL for data transformation and aggregation.

### **Insights and Findings**
   - 46% of CATEGORY2 projects were identified as "Green-Buildings." This indicates significant representation but also highlights potential for further promotion and development
   - Impact on Green Initiatives: "Green-Buildings" are a substantial component of Vancouver's sustainability efforts.
   - Encouraging greater investment in this category could enhance the city’s green goals.

### **Conclusion**
This descriptive analysis provides a detailed understanding of the important role of "Green-Buildings" in CATEGORY2 projects, supporting Vancouver’s green initiatives and guiding future efforts toward sustainability.

Design Draw io Diagram Data Analytic Platform (City of Vancouver – Domain- Greenest city projects)

![image](https://github.com/user-attachments/assets/5b876584-1bf0-42c8-b246-0019b1aa4b62)

---

## **Project 3: Diagnostic Analysis**

## Project Description
**Diagnostic Analysis of Scholar Allegations List at UCW Academic Office**  

## Project Title  
**Investigating Data Quality, Completeness, and Structure of UCW Scholar Allegations list Dataset**

## Objective  
The primary goal is to identify any anomalies, missing data, inconsistencies, or patterns in the dataset that may impact its usability for:
- Allegations list
- Visualization
- Predictive modeling
Insights from this analysis will inform necessary data cleaning and transformation steps, ensuring the dataset's readiness for downstream tasks.

## Dataset Overview  
The dataset comprises details about Allegations list in Academic Integrity at UCW.

### Dataset Fields:  
- **Student_ID**: Unique ID of the student involved in the allegation.
- **Date**: Date when the allegation was reported.
- **Type_of_Violation**: Type of academic violation (e.g., Cheating on Exam, Unauthorized Collaboration).
- **Course_Code**: Code of the course in which the violation occurred.
- **Instructor**: Name of the instructor associated with the course.
- **Severity**: Severity level of the allegation (e.g., Severe, Moderate, Minor).
- **Penalty**: Penalty imposed for the violation (e.g., Course Failure, Suspension).
- **Reported_By**: Individual or entity who reported the violation (e.g., Peer, Instructor, TA).
- **Resolution_Date**: Date when the allegation was resolved.
- **Resolution_Outcome**: Final outcome of the resolution process (e.g., Case Closed, Appeal Filed, Under Investigation).

## Methodology  

### Data Collection and Preparation  

#### **Data Generation**  
- **Simulation Design**:  
  - Dataset represents academic integrity allegations reported at UCW.
  - Simulated data includes real-world attributes such as student IDs, course codes, types of violations, penalties, and resolution outcomes.

- **Tool Used**:  
  - **ChatGPT**: Generated diverse, consistent, and realistic data entries. 

#### **Data Profiling**  
Conducted using AWS Glue DataBrew to assess data quality, structure, and completeness.

### Step 1: Data Ingestion  
1. Uploaded the raw dataset to **Amazon S3** (bucket: `aca-raw-mah`).
2. Connected the dataset to AWS Glue DataBrew for profiling.

### Step 2: Profiling Job Setup  
- Created a profiling job in AWS Glue DataBrew for column-wise analysis.
- Included all 10 columns with String Columns (8)and Integer Columns (2)

### Step 3: Profiling Insights  
1. **Data Quality**  
   - **Validity**: 100% valid values for all columns.  
   - **Missing Values**: None found (0% missing).  
   - **Outliers**: No outliers detected.  

2. **Value Distribution** 
   - **Distinct Values**:
     - Faculty_ID: 50 unique values (high cardinality),ensuring consistent identification of each student.
     - Consistent uniqueness across other fields.
   - **String Length**: Uniform distribution for text-based columns.  

3. **Top Distinct Values**  
   - Highlights the most frequent values in columns like Type_of_Violation and Course_Code 

### Step 4: Storage of Results  
- Stored profiling results in **Amazon S3** (`Data-Profiling` folder in bucket `aca-trf-mah`).  

### Step 5: Validation and Action Plan  
1. **Validation**:  
   - Dataset meets quality standards with no missing values or anomalies.  
   - Data aligns with the expected schema.  

2. **Action Plan**:  
   - No immediate cleaning required.  
   - Ready for downstream analysis (e.g., transformations, aggregations).  

## Outcome  
The UCW Allegations list dataset is complete, valid, and ready for analysis. The dataset requires no additional cleaning, ensuring a seamless transition to further analytical steps.

## Tools and Technologies  
1. **AWS Glue DataBrew**  
   - **Purpose**: Automated profiling to assess dataset quality.  
   - **Key Features**:  
     - Data Quality Metrics: Valid, invalid, and missing values.  
     - Column Profiling: Unique values, distributions, and consistency checks.  
     - Insights Panel: Cardinality, outliers, and top distinct values.  

2. **Amazon S3**  
   - **Purpose**: Centralized storage for raw data and profiling results.  
   - **Key Features**:  
     - Raw Data Storage: Original dataset.  
     - Profiling Results: Stored in the `Data-Profiling` folder.  

## Deliverables  

1. **Data Profiling Report**  
   - Comprehensive report with:  
     - Data Quality Metrics  
     - Column Statistics (value distributions, string lengths)  
     - Schema Validation  

2. **Data Quality Insights**  
   - All columns validated with 100% valid data and no anomalies.  
   - High cardinality for Faculty_ID ensures unique identification.  

3. **Profiling Results Storage**  
   - S3 Folder: `Data-Profiling` within the `ac-trf-llk` bucket.  

4. **Data Visualization**  
   - Visual summaries generated by AWS Glue DataBrew:  
     - **Bar Charts**: Value distributions for key columns.  
     - **Top Distinct Values**: Most frequent values for each column.

**Design**

Draw io Diagram Data Analytic Platform (Allegations UCW Dataset)

![image](https://github.com/user-attachments/assets/1d1180ed-6095-476c-9887-285a0ef31f7e)

Data Profiling Screen AWS Glue Brew

![image](https://github.com/user-attachments/assets/0b398013-51b7-4d49-b502-b23ef096e689)

---

## Project 4: Data Wrangling

## **Project Title**
**Data Wrangling for Student list at UCW**

## **Objective**
The objective of this project is to perform a thorough data wrangling process on the UCW Student List dataset to ensure data accuracy, standardization, and usability for academic management, reporting, and analysis. The goal is to address any data inconsistencies, missing values, or formatting issues while transforming the dataset for insights such as student enrollment trends, program distributions, and performance tracking. This ensures the dataset is optimized for decision-making, visualizations, and seamless integration into institutional systems.

## **Dataset**
The dataset contains information about student lists. Here are the key fields:

- **Student_ID**: Unique identifier for each student (String)
- **Student_Name**: Full name of the student (String)
- **Program_Enrolled**: Program or degree the student is pursuing (String)
- **Enrollment_Year**: Year the student enrolled at UCW (Integer)
- **Credits_Completed**: Number of academic credits completed by the student (Integer)
- **GPA**: Grade Point Average of the student (Decimal)
- **Email_Address**: Contact email of the student (String)
- **Status**: Enrollment status (e.g., Active, Graduated, Withdrawn) (String)

## **Methodology**

### **Step 1: Data Ingestion**
1. **Raw Data Storage**:
   - Uploaded the raw dataset to **Amazon S3** in the `aca-raw-mah` bucket.
   - Organized data using a folder structure (e.g., programs) for easy access.
2. **Configuration**:
   - Stored raw data with metadata, such as `Program_Enrolled`, `Enrollment_Year`, and `Credits_Completed`.
   - Assigned the **S3 Standard** storage class to ensure high performance for active data.


### **Step 2: Data Profiling**
1. **Profiling Job**:
   - Created a profiling job (`aca-prf-job-mah`) in **AWS Glue DataBrew** to evaluate the raw data.
   - Generated insights into:
     - Null and missing values.
     - Data type inconsistencies.
     - Frequency distributions for categorical columns.
2. **Key Findings**:
   - Detected columns with inconsistent formats (e.g., dates).
   - Identified missing values 

### **Step 3: Data Cleaning**
1. **Cleaning Job**:
   - Created a cleaning project (`aca-clnstr-job-mah`) in **AWS Glue DataBrew**.
   - Applied transformations, such as:
     - **Standardizing Column Names**: Renamed columns to adhere to a consistent naming convention.
     - **Filling Missing Values**:
       - Replaced missing categorical values with "Not Specified."
       - Imputed missing numeric values (e.g., funding amounts) using the median of relevant groups.
     - **Date Formatting**: Standardized dates to `YYYY-MM-DD` format.
2. **Output Storage**:
   - Saved cleaned data in the `aca-trf-mah` bucket:
     - **CSV** format for user accessibility.
     - **Parquet** format (with Snappy compression) for efficient storage and querying.

### **Step 4: Data Transformation**
1. **ETL Pipeline**:
   - Built an **AWS Glue ETL job** (`ACA-AI-ETL-NISHA`) for advanced transformations:
     - Filtered and Aggregated data to calculate totals and averages by programs enrolled and year enrolled.
     - Derived new columns.
2. **Output Storage**:
   - Transformed data was stored in **S3** (`aca-trf-mah`) for further reporting and visualization.


### **Step 5: Data Validation**
1. **Validation Job**:
   - Ran a final data profiling job to ensure all cleaning and transformations were applied correctly.
   - Verified the integrity of cleaned and transformed data.

## **Tools and Technologies**

### **AWS Tools Used**
1. **Amazon S3**:
   - Centralized storage for raw, cleaned, and transformed data.
   - Lifecycle rules to archive inactive data.
2. **AWS Glue DataBrew**:
   - Data profiling and cleaning jobs to standardize and validate the dataset.
3. **AWS Glue (ETL Jobs)**:
   - Built advanced ETL pipelines for filtering, aggregations, and data transformations.

## **Deliverables**

1. **Cleaned Dataset**  
   - A cleaned and standardized version of the UCW students List dataset stored in:
     - **CSV** format for ease of access.
     - **Parquet** format for optimized storage and querying.

2. **Transformed Dataset**  
   - Aggregated and derived metrics stored in S3 for reporting, such as:
     - Total and average funding by department.
     - Research activity trends over time.

3. **Data Profiling Reports**  
   - Reports generated by **AWS Glue DataBrew**, detailing:
     - Data quality metrics.
     - Distribution of values for key columns.
     - Anomalies and missing data.

4. **ETL Pipeline**  
   - An **AWS Glue ETL pipeline** that automates the transformation of research data, enabling efficient reuse for periodic updates.

**Design**

Draw io Diagram Data Analytic Platform (student List UCW Dataset)

![image](https://github.com/user-attachments/assets/69b7246f-c969-4506-b7b8-d069045af252)


## **Conclusion**
This project establishes a robust workflow for wrangling research data, ensuring it is analysis-ready and aligned with academic reporting requirements. By leveraging AWS tools, the process ensures scalability, efficiency, and reliability for managing student list data at UCW.

## Project 5: Data Quality

**Project Title:**  

### Data Quality Control for the Greenest city project Dataset 

**Project Description:**  
The project integrates data quality control measures within a robust data pipeline hosted on AWS, designed for the City of Vancouver Greenest city project. The system ensures the reliability, accuracy, and consistency of the dataset, leveraging scalable cloud-based services to streamline data ingestion, transformation, validation, and monitoring.

### Data Pipeline Overview
Based on the provided architecture diagram, the data pipeline for the parking ticket dataset is structured as follows:

#### **1. Data Ingestion and Storage**
- **Source:** The data team accesses Greenest city project data via the internet, which is stored in **Amazon S3** buckets (`trf-data-nisha`).
- **Security:** Data is encrypted using AWS Key Management Service (KMS) with `cov-gcp-key-nisha` for secure storage.


#### **2. ETL Processing**
- **AWS Glue Jobs:**  
  - Multiple AWS Glue jobs are orchestrated for ETL tasks:
    - Extract raw data from S3 buckets.
    - Transform the data by removing duplicates, standardizing formats, and imputing missing values.
    - Load the cleansed data back into S3 (`cov-gcp-datacatalog-nisha`) for further analysis.

- **Transformation Logic:**  
  - Applied using AWS Glue transformations to adhere to predefined data quality rules.

#### **3. Data Cataloging and Querying**
- **AWS Glue Data Catalog:**  
  - Metadata is maintained in AWS Glue's Data Catalog (`cov-gcp-datacatalog-nisha`) to ensure seamless integration with analytics tools.  
  - This enables efficient querying and exploration of structured datasets.

- **Amazon Athena:**  
  - Utilized to run SQL queries on the cleansed data stored in S3.  
  - Queries validate data quality metrics (e.g., uniqueness, completeness) and generate analytical insights.

#### **4. Validation and Reporting**
- **SQL Query Outputs:**  
  - Query results are validated against predefined KPIs and metrics (e.g., missing value rate <5%, duplicates = 0).  
  - Outputs are stored in a secondary S3 bucket (`gcp-cur-nisha`).

#### **5. Monitoring and Security**
- **Amazon CloudWatch:**  
  - Real-time monitoring of data pipeline activities.  
  - Tracks ETL job status, error logs, and overall data quality trends.

- **Amazon CloudTrail:**  
  - Auditing is implemented to track access and changes to the data pipeline.  

- **KMS Integration:**  
  - Ensures data at rest and in transit is encrypted, maintaining security compliance.

#### **6. Dashboard and Reporting**
- **Visualization Tools:**  
  - A dashboard (`cov-gcp-DAP-Dash-nisha`) is implemented to provide insights into data quality metrics, job execution status, and KPIs.

### Data Quality Control Measures (Detailed Implementation)
**1. Current State Assessment:**  
   - Identified data inconsistencies during ingestion (e.g., missing fields and invalid formats).  
   - Integrated monitoring tools to log pipeline performance and highlight irregularities.  

**2. Data Profiling:**  
   - AWS Glue Data Catalog provides metadata profiling for fields such as MAP ID, category2, and geo location.  

**3. Data Cleansing:**  
   - SQL scripts and Glue transformations remove duplicates, correct invalid data, and standardize field formats.  

**4. Validation Rules:**  
   - Athena SQL queries check data integrity post-transformation:
     - Map IDs are unique.
     - Missing critical fields are flagged for manual review.  

**5. Monitoring and Reporting:**  
   - CloudWatch dashboards offer real-time monitoring of ETL jobs.  
   - Alerts are configured for anomalies like job failures or data deviations.

### Deliverables
- A secure and reliable data pipeline for the greenest city project dataset.  
- Real-time dashboard visualizing data quality metrics and trends.  
- Comprehensive documentation of the ETL process and validation framework.  
- Cleaned and validated dataset ready for analysis and reporting.  

**Design**

Draw io Diagram Data Analytic Platform (City of Vancouver - Parking Tikcet Dataset )

![image](https://github.com/user-attachments/assets/127de84f-9a25-45c8-9de2-82cdc51fb8be)
