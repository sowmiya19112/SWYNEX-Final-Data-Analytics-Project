**DATA DICTIONARY**

**Student Performance Analytics**

**SWYNEX Technologies – Internship Task 4**



**1. Introduction**



This document provides a detailed description of the dataset used in the Student Performance Analytics project.



A data dictionary is a structured reference that explains the meaning, characteristics, expected data types, and analytical relevance of each column in a dataset.



It helps analysts and stakeholders understand the dataset before performing data cleaning, SQL queries, exploratory data analysis, and dashboard development.



The dataset contains student-related academic, demographic, behavioral, and environmental information that can be explored to understand variations in examination performance.



**2. Dataset Overview**



| Attribute | Description |

|---|---|

| Dataset Name | Student Performance Dataset |

| File Name | cleaned\_student\_data.csv |

| Total Records | 6,607 |

| Total Columns | 20 |

| File Format | CSV |

| Domain | Education Analytics |

| Target Variable | Exam\_Score |

| Data Status | Cleaned Dataset |



**3. Dataset Column Classification**



The 20 columns can be organized into the following analytical categories.



**3.1 Academic Performance Attributes**



These attributes describe students' academic preparation and examination outcomes.



\- Hours\_Studied

\- Previous\_Scores

\- Tutoring\_Sessions

\- Exam\_Score



**3.2 Student Behavioral Attributes**



These attributes represent student habits and activities that can be explored in relation to academic outcomes.



\- Attendance

\- Sleep\_Hours

\- Extracurricular\_Activities

\- Physical\_Activity

\- Motivation\_Level



**3.3 Family and Socioeconomic Attributes**



These attributes describe the student's family background and educational environment.



\- Parental\_Involvement

\- Family\_Income

\- Parental\_Education\_Level



**3.4 Educational Environment Attributes**



These attributes represent the resources and conditions associated with the student's learning environment.



\- Access\_to\_Resources

\- Teacher\_Quality

\- School\_Type

\- Internet\_Access

\- Peer\_Influence

\- Distance\_from\_Home



**3.5 Student Demographic and Learning Attributes**



These attributes provide additional information about student characteristics and learning requirements.



\- Gender

\- Learning\_Disabilities







**4. Detailed Column Descriptions**

**4.1 Academic Performance Attributes**



**1. Hours\_Studied**



\- Expected Data Type: Numeric

\- Description: Represents the number of hours a student spends studying.

\- Analytical Purpose: Helps examine the relationship between study time and examination performance.

\- Business Relevance: Can help identify whether students who dedicate more time to studying demonstrate different academic outcomes.



\*\***2. Previous\_Scores**\*\*



\- Expected Data Type: Numeric

\- Description: Represents the student's previous academic examination scores.

\- Analytical Purpose: Used to compare previous academic performance with current examination results.

\- Business Relevance: Helps understand performance consistency and changes in academic achievement.



**3. Tutoring\_Sessions**



\- Expected Data Type: Numeric / Integer

\- Description: Represents the number of tutoring sessions attended by a student.

\- Analytical Purpose: Helps explore the relationship between additional academic support and examination scores.

\- Business Relevance: Provides an opportunity to evaluate patterns associated with supplementary learning support.



**4. Exam\_Score**



\- Expected Data Type: Numeric

\- Description: Represents the student's examination score.

\- Analytical Purpose: Serves as the primary outcome variable for student performance analysis.

\- Business Relevance: Helps evaluate overall academic achievement and compare examination performance across different student groups.



**4.2 Student Behavioral Attributes**



**5. Attendance**



\- Expected Data Type: Numeric

\- Description: Represents the student's attendance level.

\- Analytical Purpose: Helps examine the relationship between classroom attendance and examination scores.

\- Business Relevance: Supports the identification of attendance-related performance patterns.



**6. Sleep\_Hours**



\- Expected Data Type: Numeric

\- Description: Represents the average number of hours a student sleeps.

\- Analytical Purpose: Helps explore whether sleep duration is associated with differences in academic performance.

\- Business Relevance: Provides insights into the relationship between student lifestyle patterns and learning outcomes.



**7. Extracurricular\_Activities**



\- Expected Data Type: Categorical

\- Description: Indicates whether a student participates in extracurricular activities.

\- Analytical Purpose: Enables comparison of academic performance between participation groups.

\- Business Relevance: Helps examine the relationship between activities outside regular academics and examination outcomes.



**8. Motivation\_Level**



\- Expected Data Type: Categorical

\- Description: Represents the student's motivation level.

\- Analytical Purpose: Helps compare academic performance across different motivation categories.

\- Business Relevance: Supports the exploration of motivational factors associated with student learning outcomes.



**9. Physical\_Activity**



\- Expected Data Type: Numeric

\- Description: Represents the student's physical activity level.

\- Analytical Purpose: Helps investigate potential relationships between physical activity and academic performance.

\- Business Relevance: Allows exploration of lifestyle and academic performance patterns.



**4.3 Family and Socioeconomic Attributes**



**10. Parental\_Involvement**



\- Expected Data Type: Categorical

\- Description: Represents the level of parental involvement in the student's education.

\- Analytical Purpose: Helps compare examination performance across different parental involvement levels.

\- Business Relevance: Provides insights into the potential relationship between family support and student achievement.



**11. Family\_Income**



\- Expected Data Type: Categorical

\- Description: Represents the income category of the student's family.

\- Analytical Purpose: Enables comparison of academic outcomes across different family income groups.

\- Business Relevance: Helps explore socioeconomic differences in student performance.



**12. Parental\_Education\_Level**



\- Expected Data Type: Categorical

\- Description: Represents the educational qualification level of the student's parents.

\- Analytical Purpose: Helps investigate whether parental education categories are associated with differences in student examination outcomes.

\- Business Relevance: Supports understanding of family educational background in relation to academic achievement.



**4.4 Educational Environment Attributes**



**13. Access\_to\_Resources**



\- Expected Data Type: Categorical

\- Description: Represents the student's level of access to educational resources.

\- Analytical Purpose: Helps compare student performance across resource accessibility categories.

\- Business Relevance: Helps explore the importance of learning resources in educational environments.



**14. Teacher\_Quality**



\- Expected Data Type: Categorical

\- Description: Represents the quality category of teaching available to students.

\- Analytical Purpose: Allows examination of academic performance across teacher quality categories.

\- Business Relevance: Supports analysis of the relationship between teaching conditions and student outcomes.



**15. School\_Type**



\- Expected Data Type: Categorical

\- Description: Identifies the type of school attended by the student.

\- Analytical Purpose: Enables performance comparisons between school categories.

\- Business Relevance: Helps examine variations in student outcomes across different school environments.



**16. Internet\_Access**



\- Expected Data Type: Categorical

\- Description: Indicates whether the student has access to the internet.

\- Analytical Purpose: Helps explore differences in academic performance based on internet accessibility.

\- Business Relevance: Provides an opportunity to understand the role of digital access in students' learning environments.



**17. Peer\_Influence**



\- Expected Data Type: Categorical

\- Description: Represents the influence of peers on the student's learning environment.

\- Analytical Purpose: Helps compare examination performance across peer influence categories.

\- Business Relevance: Supports exploration of how the surrounding peer environment may relate to academic outcomes.



**18. Distance\_from\_Home**



\- Expected Data Type: Categorical

\- Description: Represents the distance category between the student's home and educational institution.

\- Analytical Purpose: Helps examine whether commuting distance categories are associated with variations in examination performance.

\- Business Relevance: Provides insights into potential relationships between accessibility and academic outcomes.



**4.5 Student Demographic and Learning Attributes**



**19. Gender**



\- Expected Data Type: Categorical

\- Description: Represents the gender category recorded for each student.

\- Analytical Purpose: Enables comparison of academic performance across gender categories.

\- Business Relevance: Supports demographic analysis of examination outcomes.



**20. Learning\_Disabilities**



\- Expected Data Type: Categorical

\- Description: Indicates whether a student is recorded as having a learning disability.

\- Analytical Purpose: Allows examination of academic performance patterns across the recorded categories.

\- Business Relevance: Helps educational stakeholders explore potential differences in learning support requirements.



\---



**5. Target Variable Identification**



The primary target variable selected for this project is:



**Exam\_Score**



Exam\_Score represents the examination performance of students and serves as the main outcome measure for analytical comparisons.



The remaining 19 columns act as explanatory attributes that can be explored to understand patterns and possible associations with examination performance.



This does not establish that any individual attribute directly causes a change in examination scores.



**6. Data Type Classification**



For analytical purposes, the dataset columns are classified into two broad groups.



**Numeric Attributes**



1\. Hours\_Studied

2\. Attendance

3\. Sleep\_Hours

4\. Previous\_Scores

5\. Tutoring\_Sessions

6\. Physical\_Activity

7\. Exam\_Score



**Categorical Attributes**



1\. Parental\_Involvement

2\. Access\_to\_Resources

3\. Extracurricular\_Activities

4\. Motivation\_Level

5\. Internet\_Access

6\. Family\_Income

7\. Teacher\_Quality

8\. School\_Type

9\. Peer\_Influence

10\. Learning\_Disabilities

11\. Parental\_Education\_Level

12\. Distance\_from\_Home

13\. Gender





**7. Data Quality Considerations**



The following data quality aspects are important when working with this dataset:



\- Verify that all 20 columns are correctly identified.

\- Check for missing or null values.

\- Identify duplicate student records.

\- Validate numeric columns for unexpected values.

\- Check categorical columns for inconsistent labels.

\- Verify that examination scores contain valid values.

\- Ensure consistent formatting across all columns.

\- Confirm that the cleaned dataset is suitable for further analysis.



**8. Analytical Applications**



The dataset supports several analytical activities:



1\. Study time versus examination performance analysis.

2\. Attendance and academic achievement analysis.

3\. Previous scores versus current examination scores.

4\. Parental involvement and student performance comparison.

5\. Family income and academic performance analysis.

6\. Internet access and educational performance comparison.

7\. Motivation level and examination outcome analysis.

8\. Tutoring sessions and student performance analysis.

9\. School type and academic performance comparison.

10\. Student lifestyle and academic performance exploration.



These analyses help identify patterns and generate evidence-based observations.



**9. Conclusion**



This data dictionary provides a detailed reference for all 20 attributes included in the Student Performance Dataset.



Understanding these attributes is essential for maintaining consistency throughout the data analytics workflow.



The documented column descriptions support the next stages of the project, including SQL-based analysis, Python exploratory data analysis, and Power BI dashboard development.







**Project:** Student Performance Analytics



**Organization:** SWYNEX Technologies



**Internship:** Task 4 – Final Data Analytics Project



**Dataset:** cleaned\_student\_data.csv



