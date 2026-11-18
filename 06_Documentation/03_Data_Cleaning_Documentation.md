**DATA CLEANING AND PREPARATION**

**Student Performance Analytics**

**SWYNEX Technologies – Internship Task 4**



\---



**1. Introduction**



Data cleaning and preparation is one of the most important stages in the data analytics lifecycle.



Raw datasets may contain missing values, duplicate records, inconsistent categorical values, incorrect data entries, and other data quality issues that can affect the reliability of analytical results.



In this project, MySQL was used to inspect, validate, and prepare the Student Performance Dataset before performing Exploratory Data Analysis and developing the Power BI dashboard.



The primary objective of this stage was to improve data consistency, identify data quality issues, and create a separate cleaned dataset for subsequent analysis.



**2. Dataset Overview**



The project uses a Student Performance Dataset containing academic, demographic, behavioral, family, and educational environment attributes.



| Attribute | Details |

|---|---|

| Dataset Name | Student Performance Dataset |

| Source Table | raw\_student\_data |

| Cleaned Table | cleaned\_student\_data |

| Database | swynex\_data\_cleaning |

| Total Columns | 20 |

| Dataset Records | 6,607 |

| Database | MySQL |

| Output Format | CSV |

| Final Dataset | cleaned\_student\_data.csv |



**3. Tools and Technologies**



**MySQL**



MySQL was used as the primary database management system for inspecting, validating, and preparing the dataset.



**SQL**



SQL statements were used to perform data inspection, missing-value identification, duplicate checks, categorical validation, data standardization, and numeric range validation.



**SQL Operations Use**d



\- USE

\- SHOW TABLES

\- SELECT

\- COUNT()

\- DESCRIBE

\- SUM()

\- IS NULL

\- TRIM()

\- DISTINCT

\- GROUP BY

\- HAVING

\- UNION ALL

\- MIN()

\- MAX()

\- ORDER BY

\- LIMIT

\- CREATE TABLE

\- UPDATE



**4. Data Cleaning Objectives**



The main objectives of data cleaning were:



1\. Understand the structure of the raw dataset.

2\. Verify the total number of records and columns.

3\. Identify missing and empty values.

4\. Investigate potential duplicate records.

5\. Examine categorical values for inconsistencies.

6\. Standardize selected blank categorical fields.

7\. Validate numerical columns using minimum and maximum values.

8\. Identify examination scores exceeding the expected range.

9\. Create a separate cleaned table for further analysis.

10\. Validate the prepared dataset before exporting it.



**5. Initial Data Inspection**



The first stage involved connecting to the project database and examining the raw student dataset.



**5.1 Selecting the Database**



```sql

USE swynex\_data\_cleaning;

```



This statement selects the database containing the student performance data.



**5.2 Checking Available Tables**



```sql

SHOW TABLES;

```



This command displays the tables available in the selected database.



**5.3 Inspecting the Dataset**



```sql

SELECT \*

FROM raw\_student\_data

LIMIT 10;

```



The query retrieves the first ten records to understand the structure and values of the dataset.



**5.4 Checking Total Records**



```sql

SELECT COUNT(\*) AS total\_records

FROM raw\_student\_data;

```



This query calculates the total number of records in the raw dataset.



**5.5 Identifying Column Names and Data Types**



```sql

DESCRIBE raw\_student\_data;

```



This command provides information about the column names, data types, nullability, and other table properties.



**Purpose:**



Initial inspection helps understand the dataset before applying any cleaning operations.



**6. Missing Value Analysis**



Missing-value analysis was performed to identify incomplete records and determine which columns required additional attention.



**6.1 Initial Missing Value Check**



The initial inspection focused on selected numeric and categorical columns.



```sql

SELECT

&#x20;   SUM(Hours\_Studied IS NULL) AS missing\_hours,

&#x20;   SUM(Attendance IS NULL) AS missing\_attendance,

&#x20;   SUM(Parental\_Involvement IS NULL) AS missing\_parental,

&#x20;   SUM(Access\_to\_Resources IS NULL) AS missing\_resources,

&#x20;   SUM(Extracurricular\_Activities IS NULL) AS missing\_activities,

&#x20;   SUM(Sleep\_Hours IS NULL) AS missing\_sleep,

&#x20;   SUM(Previous\_Scores IS NULL) AS missing\_previous\_scores

FROM raw\_student\_data;

```



The SUM() function was combined with IS NULL to count missing values in individual columns.



**6.2 Comprehensive Missing Value Assessment**



A broader validation query was executed on the cleaned table to inspect missing and blank values across all 20 columns.



Example:



```sql

SELECT

&#x20;   SUM(Teacher\_Quality IS NULL

&#x20;       OR TRIM(Teacher\_Quality) = '') AS missing\_teacher\_quality,



&#x20;   SUM(Parental\_Education\_Level IS NULL

&#x20;       OR TRIM(Parental\_Education\_Level) = '') AS missing\_parent\_education,



&#x20;   SUM(Distance\_from\_Home IS NULL

&#x20;       OR TRIM(Distance\_from\_Home) = '') AS missing\_distance,



&#x20;   SUM(Exam\_Score IS NULL) AS missing\_exam\_score



FROM cleaned\_student\_data;

```



The complete SQL script contains the corresponding checks for all 20 attributes.



\*\*Technical Explanation:\*\*



\- IS NULL identifies database NULL values.

\- TRIM() removes leading and trailing whitespace when checking text values.

\- Empty strings are checked separately because an empty string is not the same as SQL NULL.

\- SUM() aggregates the resulting Boolean conditions to calculate the number of affected records.



**6.3 Handling Missing and Empty Values**



The cleaning process identified empty categorical values in selected columns.



Instead of removing those records, the following descriptive category was used:



`Unknown`



This preserves the records while clearly indicating that the original category was unavailable.



**7. Duplicate Record Analysis**



Potential duplicate records were investigated using all 20 dataset columns.



**7.1 Total Record Count**



```sql

SELECT COUNT(\*) AS total\_rows

FROM raw\_student\_data;

```



This query establishes the number of rows before duplicate investigation.



**7.2 Identifying Duplicate Groups**



```sql

SELECT COUNT(\*) AS duplicate\_groups

FROM (

&#x20;   SELECT

&#x20;       Access\_to\_Resources,

&#x20;       Attendance,

&#x20;       Distance\_from\_Home,

&#x20;       Exam\_Score,

&#x20;       Extracurricular\_Activities,

&#x20;       Family\_Income,

&#x20;       Gender,

&#x20;       Hours\_Studied,

&#x20;       Internet\_Access,

&#x20;       Learning\_Disabilities,

&#x20;       Motivation\_Level,

&#x20;       Parental\_Education\_Level,

&#x20;       Parental\_Involvement,

&#x20;       Peer\_Influence,

&#x20;       Physical\_Activity,

&#x20;       Previous\_Scores,

&#x20;       School\_Type,

&#x20;       Sleep\_Hours,

&#x20;       Teacher\_Quality,

&#x20;       Tutoring\_Sessions

&#x20;   FROM raw\_student\_data

&#x20;   GROUP BY

&#x20;       Access\_to\_Resources,

&#x20;       Attendance,

&#x20;       Distance\_from\_Home,

&#x20;       Exam\_Score,

&#x20;       Extracurricular\_Activities,

&#x20;       Family\_Income,

&#x20;       Gender,

&#x20;       Hours\_Studied,

&#x20;       Internet\_Access,

&#x20;       Learning\_Disabilities,

&#x20;       Motivation\_Level,

&#x20;       Parental\_Education\_Level,

&#x20;       Parental\_Involvement,

&#x20;       Peer\_Influence,

&#x20;       Physical\_Activity,

&#x20;       Previous\_Scores,

&#x20;       School\_Type,

&#x20;       Sleep\_Hours,

&#x20;       Teacher\_Quality,

&#x20;       Tutoring\_Sessions

&#x20;   HAVING COUNT(\*) > 1

) AS duplicate\_records;

```



**Technical Explanation:**



\- GROUP BY groups records with identical values across the selected columns.

\- HAVING COUNT(\*) > 1 identifies groups appearing more than once.

\- The outer COUNT(\*) calculates the number of duplicate groups.



**Important Note:**



This query identifies duplicate groups, not the total number of duplicate rows.



The SQL script performs duplicate identification, but it does not contain a DELETE statement to remove duplicate records. Therefore, this documentation does not claim that duplicate records were deleted.



**8. Categorical Data Validation**



Categorical validation was performed to inspect the available values in selected columns.



**8.1 Checking Distinct Values**



```sql

SELECT DISTINCT Gender

FROM raw\_student\_data;



SELECT DISTINCT Parental\_Involvement

FROM raw\_student\_data;



SELECT DISTINCT Access\_to\_Resources

FROM raw\_student\_data;



SELECT DISTINCT Teacher\_Quality

FROM raw\_student\_data;



SELECT DISTINCT Distance\_from\_Home

FROM raw\_student\_data;

```



These queries identify the unique categories present in the selected columns.



**8.2 Checking Category Frequencies**



```sql

SELECT

&#x20;   'Gender' AS column\_name,

&#x20;   Gender AS value,

&#x20;   COUNT(\*) AS total

FROM raw\_student\_data

GROUP BY Gender



UNION ALL



SELECT

&#x20;   'Parental\_Involvement',

&#x20;   Parental\_Involvement,

&#x20;   COUNT(\*)

FROM raw\_student\_data

GROUP BY Parental\_Involvement;

```



The same approach was applied to other selected categorical attributes.



**Purpose:**



\- Understand category distributions.

\- Identify unexpected or empty values.

\- Review category consistency.

\- Prepare categorical fields for subsequent analysis.



**9. Creating the Cleaned Dataset**



A separate table was created to preserve the original raw dataset.



```sql

CREATE TABLE cleaned\_student\_data AS

SELECT \*

FROM raw\_student\_data;

```



**Explanation:**



The CREATE TABLE AS SELECT statement creates a new table using the records and columns from the raw table.



This approach allows cleaning operations to be performed separately without directly modifying the original source table.



**Tables Used:**



| Table | Purpose |

|---|---|

| raw\_student\_data | Original imported dataset |

| cleaned\_student\_data | Separate table used for cleaning operations |



**10. Handling Empty Categorical Values**



Selected categorical columns contained empty string values.



These values were standardized using the label 'Unknown'.



**10.1 Cleaning Teacher Quality**



```sql

UPDATE cleaned\_student\_data

SET Teacher\_Quality = 'Unknown'

WHERE TRIM(Teacher\_Quality) = '';

```



This query replaces empty or whitespace-only Teacher\_Quality values with 'Unknown'.



**10.2 Cleaning Parental Education Level**



```sql

UPDATE cleaned\_student\_data

SET Parental\_Education\_Level = 'Unknown'

WHERE TRIM(Parental\_Education\_Level) = '';

```



This operation standardizes empty values in the parental education column.



**10.3 Cleaning Distance from Home**



```sql

UPDATE cleaned\_student\_data

SET Distance\_from\_Home = 'Unknown'

WHERE Distance\_from\_Home IS NOT NULL

AND TRIM(Distance\_from\_Home) = '';

```



This operation replaces non-NULL empty or whitespace-only values in the distance category.



**10.4 Verifying Updated Categories**



```sql

SELECT Teacher\_Quality, COUNT(\*) AS total

FROM cleaned\_student\_data

GROUP BY Teacher\_Quality;

```



Additional GROUP BY queries were used to inspect the updated categories in the relevant columns.



**Reason for Using Unknown:**



Replacing selected blank categorical values with 'Unknown' preserves the original records and avoids introducing an unsupported category assumption.



The original missing information is represented transparently rather than being replaced with an estimated value.



**11. Numerical Data Validation**



Numerical validation was performed to understand the minimum and maximum values of selected numerical attributes.



**11.1 Range Validation**



```sql

SELECT

&#x20;   MIN(Attendance) AS min\_attendance,

&#x20;   MAX(Attendance) AS max\_attendance,

&#x20;   MIN(Exam\_Score) AS min\_exam\_score,

&#x20;   MAX(Exam\_Score) AS max\_exam\_score,

&#x20;   MIN(Hours\_Studied) AS min\_hours\_studied,

&#x20;   MAX(Hours\_Studied) AS max\_hours\_studied,

&#x20;   MIN(Sleep\_Hours) AS min\_sleep\_hours,

&#x20;   MAX(Sleep\_Hours) AS max\_sleep\_hours,

&#x20;   MIN(Previous\_Scores) AS min\_previous\_scores,

&#x20;   MAX(Previous\_Scores) AS max\_previous\_scores,

&#x20;   MIN(Physical\_Activity) AS min\_physical\_activity,

&#x20;   MAX(Physical\_Activity) AS max\_physical\_activity,

&#x20;   MIN(Tutoring\_Sessions) AS min\_tutoring\_sessions,

&#x20;   MAX(Tutoring\_Sessions) AS max\_tutoring\_sessions

FROM cleaned\_student\_data;

```



\*\*Technical Explanation:\*\*



\- MIN() identifies the lowest value.

\- MAX() identifies the highest value.

\- The results help identify values that may require additional validation.



**11.2 Checking Examination Scores**



```sql

SELECT \*

FROM cleaned\_student\_data

WHERE Exam\_Score > 100;

```



This query identifies examination records with scores exceeding the expected upper limit of 100.



The analysis also inspected the frequency of high examination scores in the original dataset.



```sql

SELECT Exam\_Score, COUNT(\*) AS total\_students

FROM cleaned\_student\_data

GROUP BY Exam\_Score

ORDER BY Exam\_Score DESC

LIMIT 10;

```



This query displays the highest examination score values and their corresponding record counts.



**12. Examination Score Correction**



During examination score validation, a value of 101 was investigated as an invalid score because the expected examination score range was up to 100.



The original dataset was inspected using:



```sql

SELECT

&#x20;   Exam\_Score,

&#x20;   COUNT(\*) AS total

FROM raw\_student\_data

WHERE Exam\_Score > 100

GROUP BY Exam\_Score;

```



The SQL script then applied the following correction:



```sql

UPDATE cleaned\_student\_data

SET Exam\_Score = 100

WHERE Exam\_Score = 101

LIMIT 1;

```



**Explanation:**



The UPDATE statement changes one matching record with an examination score of 101 to 100.



The LIMIT 1 clause restricts the correction to one matching row.



**Important Data Quality Consideration:**



This is a limited correction, not a complete correction of every invalid examination score.



The appropriate treatment of other values above 100 should be determined after reviewing the original records and the dataset's scoring rules.



The original raw table remains available for reference.



**13. Final Data Validation**



After the cleaning operations, additional validation queries were executed.



**13.1 Checking Total Records**



```sql

SELECT COUNT(\*) AS total\_rows

FROM cleaned\_student\_data;

```



This query verifies the total number of records in the cleaned table.



**13.2 Rechecking Missing Values**



The comprehensive missing-value query was executed again to review NULL and empty values across the 20 columns.



**13.3 Checking Invalid Examination Scores**



```sql

SELECT COUNT(\*) AS invalid\_scores

FROM cleaned\_student\_data

WHERE Exam\_Score > 100;

```



This query calculates the number of examination scores that remain above 100.



**Additional inspection:**



```sql

SELECT \*

FROM cleaned\_student\_data

WHERE Exam\_Score > 100;

```



These validation steps help assess whether the applied corrections addressed the identified issue.



**14. Final Dataset Preparation**



After the MySQL cleaning and validation stage, the prepared dataset was made available for subsequent analytical activities.



**Final exported file:**



`cleaned\_student\_data.csv`



**Dataset details:**



| Attribute | Details |

|---|---|

| File Name | cleaned\_student\_data.csv |

| Format | CSV |

| Records | 6,607 |

| Columns | 20 |

| Database Tool | MySQL |



The CSV file is used as the input dataset for Python Exploratory Data Analysis and Power BI dashboard development.



**15. Challenges and Solutions**



**Challenge 1:** Identifying Missing Values



**Issue:** SQL NULL values and empty strings require different validation conditions.



**Solution:** IS NULL and TRIM() = '' were used to identify these conditions.



**Challenge 2:** Investigating Duplicate Records



**Issue:** Repeated records needed to be identified across multiple attributes.



**Solution:** GROUP BY and HAVING COUNT(\*) > 1 were used to identify duplicate groups.



**Challenge 3:** Inconsistent or Empty Categories



**Issue:** Empty categorical fields could affect grouping and visualization.



**Solution:** Selected empty categories were standardized using the value 'Unknown'.



**Challenge 4:** Invalid Examination Scores



**Issue:** Examination scores above the expected maximum were identified.



**Solution:** Range checks were performed, and one matching score of 101 was corrected to 100 using UPDATE with LIMIT 1.



**Challenge 5:** Preserving Original Data



**Issue:** Cleaning operations should not overwrite the original imported dataset.



**Solution:** A separate cleaned\_student\_data table was created using CREATE TABLE AS SELECT.



**16. Data Cleaning Limitations**



The following limitations should be considered:



1\. Duplicate groups were identified, but duplicate deletion was not implemented in the supplied SQL script.

2\. Empty-value standardization was applied to selected categorical columns rather than all 20 columns.

3\. The examination score correction was limited to one matching record.

4\. The SQL script contains validation queries, but their numerical result outputs are not included in this documentation.

5\. Data cleaning operations do not establish whether an observed student-related attribute causes a particular examination outcome.



These limitations are documented to maintain transparency and reproducibility.



**17. Conclusion**



The data cleaning and preparation stage established a structured foundation for the Student Performance Analytics project.



MySQL was used to inspect the raw dataset, assess data quality, investigate potential duplicate groups, validate categorical attributes, standardize selected empty values, and examine numerical ranges.



A separate cleaned table was created to preserve the original dataset while performing the required preparation operations.



The resulting CSV dataset was prepared for the next stages of the project, including Python-based Exploratory Data Analysis and Power BI dashboard development.



\---



**Project:** Student Performance Analytics



**Organization:** SWYNEX Technologies



**Internship:** Task 4 – Final Data Analytics Project



**Technology:** MySQL and SQL



**Output Dataset:** cleaned\_student\_data.csv

