**SQL DATA ANALYSIS**

**Student Performance Analytics**

**SWYNEX Technologies – Internship Task 4**



\---



**1. Introduction**



SQL-based data analysis is an important stage in the Student Performance Analytics project.



After preparing the student dataset, SQL is used to retrieve, organize, summarize, and examine relevant information from the database.



MySQL provides a structured environment for analyzing student attributes and investigating patterns associated with examination performance.



This document describes the SQL analysis methodology, analytical objectives, query techniques, and business questions relevant to the project.



**2. Analysis Objectives**



The primary objectives of SQL analysis are:



1\. Understand the distribution of student records.

2\. Calculate relevant summary statistics.

3\. Compare examination performance across student categories.

4\. Examine relationships between academic and behavioral attributes.

5\. Investigate family and educational environment factors.

6\. Identify patterns that can support further exploratory analysis.

7\. Prepare structured analytical outputs for visualization.



**3. Database Information**



| Attribute | Details |

|---|---|

| Database | swynex\_data\_cleaning |

| Original Table | raw\_student\_data |

| Prepared Table | cleaned\_student\_data |

| Records | 6,607 |

| Columns | 20 |

| Database Language | MySQL |



**4. SQL Concepts and Functions**



The following SQL concepts are relevant to the project analysis.



**4.1 SELECT**



Used to retrieve specific columns and records from the student dataset.



**4.2 WHERE**



Used to filter records based on specified conditions.



**4.3 GROUP BY**



Used to group students into categories for comparative analysis.



**4.4 ORDER BY**



Used to arrange analytical results in ascending or descending order.



**4.5 COUNT()**



Used to calculate the number of student records within a dataset or category.



**4.6 AVG()**



Used to calculate average values, including average examination scores.



**4.7 MIN() and MAX()**



Used to identify minimum and maximum values.



**4.8 SUM()**



Used to calculate aggregate totals and support conditional data checks.



**4.9 HAVING**



Used to filter grouped results based on aggregate conditions.



**4.10 CASE**



Can be used to classify student records into analytical categories based on defined conditions.



**5. Business Questions**



The SQL analysis is structured around the following business questions.



**Question 1:** What is the overall student performance?



Objective: Understand the general examination performance of the students.



Suggested metrics:

\- Total student records.

\- Average examination score.

\- Highest examination score.

\- Lowest examination score.



**Question 2:** How does study time relate to examination performance?



Objective: Examine differences in average examination scores across study-hour categories.



**Question 3:** How does attendance relate to academic performance?



Objective: Compare student examination outcomes across attendance levels.



**Question 4:** How do previous scores compare with current examination results?



Objective: Explore academic performance patterns using previous examination scores.



**Question 5:** Does parental involvement show differences in student performance?



Objective: Compare average examination scores across parental involvement categories.



**Question 6:** How does access to educational resources relate to student outcomes?



Objective: Examine examination performance across resource accessibility categories.



**Question 7:** How does motivation level vary across performance groups?



Objective: Compare academic outcomes across motivation categories.



**Question 8:** How are tutoring sessions associated with examination performance?



Objective: Examine average examination scores based on the number of tutoring sessions.



**Question 9:** Are there performance differences across school types?



Objective: Compare examination results across the available school categories.



**Question 10:** How do family income categories compare in terms of academic outcomes?



Objective: Explore the distribution of examination scores across family income groups.



**6. Analytical Query Techniques**



The following query structures can be used to answer the business questions after validating the cleaned dataset.



**6.1 Overall Performance Summary**



```sql

SELECT

&#x20;   COUNT(\*) AS total\_students,

&#x20;   ROUND(AVG(Exam\_Score), 2) AS average\_score,

&#x20;   MIN(Exam\_Score) AS minimum\_score,

&#x20;   MAX(Exam\_Score) AS maximum\_score

FROM cleaned\_student\_data;

```



**6.2 Performance by Motivation Level**



```sql

SELECT

&#x20;   Motivation\_Level,

&#x20;   COUNT(\*) AS total\_students,

&#x20;   ROUND(AVG(Exam\_Score), 2) AS average\_score

FROM cleaned\_student\_data

GROUP BY Motivation\_Level

ORDER BY average\_score DESC;

```



**6.3 Performance by School Type**



```sql

SELECT

&#x20;   School\_Type,

&#x20;   COUNT(\*) AS total\_students,

&#x20;   ROUND(AVG(Exam\_Score), 2) AS average\_score

FROM cleaned\_student\_data

GROUP BY School\_Type

ORDER BY average\_score DESC;

```



**6.4 Performance by Parental Involvement**



```sql

SELECT

&#x20;   Parental\_Involvement,

&#x20;   COUNT(\*) AS total\_students,

&#x20;   ROUND(AVG(Exam\_Score), 2) AS average\_score

FROM cleaned\_student\_data

GROUP BY Parental\_Involvement

ORDER BY average\_score DESC;

```



**6.5 Performance by Family Income**



```sql

SELECT

&#x20;   Family\_Income,

&#x20;   COUNT(\*) AS total\_students,

&#x20;   ROUND(AVG(Exam\_Score), 2) AS average\_score

FROM cleaned\_student\_data

GROUP BY Family\_Income

ORDER BY average\_score DESC;

```



**6.6 Performance by Study Hours**



```sql

SELECT

&#x20;   Hours\_Studied,

&#x20;   COUNT(\*) AS total\_students,

&#x20;   ROUND(AVG(Exam\_Score), 2) AS average\_score

FROM cleaned\_student\_data

GROUP BY Hours\_Studied

ORDER BY Hours\_Studied;

```



Note: These are analytical query templates for the project. Final results must be obtained by executing the queries against the verified cleaned dataset.



**7. SQL Analysis and Visualization**



SQL analysis outputs can be used as inputs for further analytical activities.



The results can support:



\- Python-based statistical analysis.

\- Exploratory data visualizations.

\- Power BI dashboard development.

\- Comparative performance reporting.

\- Business insight generation.



**8. Data Interpretation**



SQL aggregation results help identify differences between student categories.



However, differences in average scores should be interpreted carefully.



An observed relationship between two attributes does not automatically establish causation.



Additional statistical analysis may be required to understand the strength and significance of observed relationships.



**9. Business Value**



SQL analysis helps transform a structured student dataset into meaningful analytical summaries.



These summaries can support educational stakeholders in understanding student performance, identifying patterns, and planning further investigation into academic outcomes.



**10. Conclusion**



SQL provides an efficient method for analyzing student performance data.



Through filtering, grouping, aggregation, and comparative queries, the project establishes a structured approach to investigating academic outcomes and their relationships with student-related attributes.



The SQL analysis stage supports the next stages of the project, including Python Exploratory Data Analysis and interactive Power BI reporting.



\---



**Project:** Student Performance Analytics



**Organization:** SWYNEX Technologies



**Internship:** Task 4 – Final Data Analytics Project



**Technology:** MySQL and SQL

