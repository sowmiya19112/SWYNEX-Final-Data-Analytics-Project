**SWYNEX – FINAL DATA ANALYTICS PROJECT**



**Student Performance Analytics \& Insights**



**An End-to-End Data Analytics Case Study Using MySQL, Python, Pandas, Matplotlib \& Power BI**



**Internship:** SWYNEX Technologies  

**Task:** Task 4 – Final Data Analytics Project  

**Domain:** Education Analytics  

**Project Type:** Data Cleaning | Exploratory Data Analysis | SQL Analytics | Business Intelligence



\---



**1. Executive Summary**



Student academic performance is influenced by multiple academic, behavioral, and environmental factors. Understanding these factors can help educational institutions identify performance patterns and make informed decisions.



This project presents an end-to-end data analytics solution focused on analyzing student performance data and exploring the factors associated with academic outcomes.



The project integrates multiple data analytics technologies, including MySQL for data cleaning and querying, Python for exploratory data analysis, and Microsoft Power BI for interactive dashboard development.



The complete workflow transforms raw student information into a structured dataset, performs analytical investigations, and presents findings through visual reports.



The final objective is to demonstrate how data analytics can support educational decision-making through data-driven insights.



**2. Business Problem Statement**



Educational institutions generate large amounts of student-related data, including study hours, attendance, parental involvement, access to learning resources, sleep patterns, extracurricular activities, and previous academic performance.



However, collecting student information alone does not provide sufficient understanding of academic performance.



Institutions need to explore the relationships between these factors and student outcomes to identify patterns, understand potential areas of improvement, and support better academic planning.



**Key Business Questions**



1\. How do study hours relate to student examination performance?

2\. What patterns can be observed between attendance and academic scores?

3\. How is parental involvement associated with student performance?

4\. Does access to learning resources show any relationship with academic outcomes?

5\. What patterns exist between sleep hours and examination scores?

6\. How do extracurricular activities relate to academic performance?

7\. Which student-related factors deserve further investigation?

8\. How can performance information be presented through an interactive dashboard?



The project uses data analysis and visualization techniques to investigate these questions.



**3. Project Objectives**



The primary objectives of this project are:



**Data Preparation**

\- Understand the structure and quality of the raw dataset.

\- Identify missing and inconsistent values.

\- Detect and investigate duplicate records.

\- Validate data types and column values.

\- Prepare a structured dataset for analysis.



**Data Analysis**

\- Perform SQL-based data exploration.

\- Calculate relevant descriptive statistics.

\- Analyze student performance patterns.

\- Explore relationships between student-related factors and exam scores.



**Data Visualization**

\- Develop meaningful visualizations using Python.

\- Create an interactive Power BI dashboard.

\- Present key performance indicators.

\- Enable users to explore information through filters and slicers.



**Business Intelligence**

\- Translate analytical findings into understandable insights.

\- Identify potential areas for educational improvement.

\- Present data-driven recommendations.



**4. Dataset Information**



**Dataset Name:** Student Performance Dataset



**Cleaned Dataset:** `cleaned\_student\_data.csv`



**Domain:** Education Analytics



**Format:** CSV



**Dataset Size:** 6,607 records and 20 columns.



The dataset contains student-related information covering academic performance, study habits, attendance, and other influencing factors.



**Important Dataset Attributes**



| Attribute | Description |

|---|---|

| Hours\_Studied | Number of hours spent studying |

| Attendance | Student attendance information |

| Parental\_Involvement | Level of parental involvement |

| Access\_to\_Resources | Availability of learning resources |

| Extracurricular\_Activities | Participation in extracurricular activities |

| Sleep\_Hours | Hours of sleep |

| Previous\_Scores | Previous academic scores |

| Exam\_Score | Student examination score |



**The above attributes are selected examples of the dataset columns.**



**Dataset Preparation**



The dataset was processed before being used for exploratory analysis and dashboard development.



The cleaned CSV file is included in the project repository for reference and reproducibility.



**5. Tools and Technologies Used**



| Technology | Application |

|---|---|

| MySQL | Data cleaning, validation and SQL querying |

| Python | Exploratory data analysis |

| Pandas | Data manipulation and processing |

| Matplotlib | Statistical and graphical visualization |

| Power BI | Interactive dashboard development |

| Microsoft Excel | Dataset inspection |

| GitHub | Version control and project documentation |



**Technology Workflow**



**MySQL → Python → Power BI → Business Insights**



Each technology contributes to a different stage of the analytical workflow.



**6. Project Methodology**



The project follows a structured data analytics lifecycle.



**Phase 1 – Data Understanding**



\- Imported and inspected the student dataset.

\- Examined the dataset structure.

\- Reviewed column names and data types.

\- Identified the variables relevant to academic performance.



**Phase 2 – Data Cleaning and Preparation**



\- Checked missing values.

\- Investigated duplicate records.

\- Reviewed inconsistent data.

\- Validated important numerical and categorical fields.

\- Corrected identified data quality issues.

\- Prepared the cleaned dataset for further analysis.



**Phase 3 – SQL-Based Analysis**



\- Connected to the MySQL database.

\- Executed data inspection queries.

\- Calculated record counts.

\- Examined missing values.

\- Performed data validation.

\- Developed queries for analytical investigation.



**Phase 4 – Exploratory Data Analysis**



\- Loaded the cleaned dataset using Pandas.

\- Inspected dataset dimensions and data types.

\- Performed descriptive statistical analysis.

\- Explored distributions and relationships.

\- Generated visualizations using Matplotlib.



**Phase 5 – Dashboard Development**



\- Imported the prepared dataset into Power BI.

\- Developed KPI cards.

\- Created interactive charts.

\- Added slicers for data exploration.

\- Implemented reset-filter functionality.

\- Organized the dashboard for easier interpretation.



**Phase 6 – Business Insights**



\- Reviewed analytical outputs.

\- Identified meaningful patterns.

\- Interpreted relevant performance indicators.

\- Prepared recommendations based on validated findings.



**7. Data Cleaning and Preparation Using MySQL**



Data quality is an important part of every analytical project.



Before performing analysis, the dataset was inspected and processed using MySQL.



**Data Cleaning Activities**



**7.1 Dataset Inspection**



The initial dataset was examined to understand:

\- Total number of records.

\- Available columns.

\- Column data types.

\- General data structure.



**7.2 Missing Value Analysis**



Missing values were investigated across relevant dataset columns.



This helped identify incomplete records and understand the quality of the source data.



**7.3 Duplicate Record Validation**



Duplicate records were investigated to avoid potential inconsistencies during analysis.



**7.4 Data Validation**



Important fields were checked for appropriate values and consistency.



**7.5 Final Dataset Preparation**



The processed dataset was prepared and exported as:



`cleaned\_student\_data.csv`



The cleaned dataset was subsequently used for Python analysis and Power BI dashboard development.



**8. SQL Analysis**



MySQL was used to perform data exploration, validation, and analytical querying.



**SQL Concepts Applied**



\- SELECT statements

\- WHERE conditions

\- COUNT() functions

\- SUM() functions

\- GROUP BY

\- Aggregate functions

\- NULL value checks

\- DESCRIBE statements

\- Data validation queries



**Analytical Objectives**



1\. Understand the dataset structure.

2\. Calculate total records.

3\. Inspect column information.

4\. Identify missing values.

5\. Validate the cleaned dataset.

6\. Investigate student performance indicators.



The SQL source files are maintained in the `02\_SQL\_Analysis` directory.



**9. Exploratory Data Analysis Using Python**



Exploratory Data Analysis (EDA) was performed to understand the distribution, structure, and relationships within the student dataset.



**Libraries Used**



**Pandas**

\- Data loading.

\- Data inspection.

\- Data manipulation.

\- Statistical summaries.



**Matplotlib**

\- Distribution visualizations.

\- Comparison charts.

\- Analytical plots.



**EDA Activities**



\- Dataset overview.

\- Statistical summary.

\- Variable distribution analysis.

\- Categorical variable exploration.

\- Numerical variable analysis.

\- Student performance exploration.

\- Relationship analysis between relevant variables.



**Key Areas Investigated**



\- Study hours and examination scores.

\- Attendance and academic performance.

\- Previous scores and current examination performance.

\- Parental involvement.

\- Learning resource availability.

\- Sleep hours.

\- Extracurricular participation.



Generated EDA visualizations are included in the project directory.



**10. Power BI Dashboard Development**



An interactive Student Performance Analytics Dashboard was developed using Microsoft Power BI.



The dashboard converts analytical information into an easy-to-understand visual reporting experience.



**Dashboard Components**



**KPI Cards**



The dashboard contains six KPI cards to provide a summarized view of important performance indicators.



**Data Visualizations**



Eight visualizations are included to explore student performance and related factors.



**Interactive Slicers**



Five slicers allow users to filter and explore the dataset based on available categories.



**Reset Filters Functionality**



Bookmark-based reset functionality was implemented to restore the dashboard to its default filter state.



**Dashboard Features**



\- Interactive filtering.

\- KPI-based performance overview.

\- Multiple visualization types.

\- Dynamic data exploration.

\- Reset filters functionality.

\- Organized dashboard layout.



**Dashboard Screenshot**



The dashboard preview is available in:



`05\_Screenshots/`



**Power BI Project File**



The complete editable dashboard file is available in:



`04\_PowerBI\_Dashboard/`



**11. Key Business Questions and Analytical Interpretation**



The project investigates several important questions related to student performance.



| Business Question | Analytical Approach |

|---|---|

| Does study time relate to exam performance? | Compare study hours and exam scores |

| Is attendance associated with academic outcomes? | Examine attendance and score patterns |

| Does parental involvement matter? | Compare performance across involvement categories |

| Are learning resources relevant? | Explore resource availability and exam scores |

| Does sleep duration show a pattern? | Examine sleep hours and performance |

| Do previous scores relate to current scores? | Compare previous and current examination scores |



The final interpretations should be supported by the actual SQL queries, Python outputs, and Power BI results.



**12. Business Insights**



The main purpose of this analysis is to identify useful patterns from student-related data.



The following areas are considered for business interpretation:



**Academic Performance**

Understand the distribution of examination scores and identify performance patterns.



**Study Habits**

Explore how study hours are associated with academic performance.



**Attendance Patterns**

Investigate attendance-related differences in student outcomes.



**Parental Involvement**

Examine performance across different parental involvement categories.



**Learning Resources**

Explore whether differences in resource availability correspond with performance differences.



**Student Well-being**

Investigate sleep duration and other relevant student-related variables.



**Important:** Specific numerical findings, strongest relationships, and final conclusions must be inserted after validating the actual analysis outputs. Association does not automatically establish causation.



**13. Business Recommendations**



Based on the validated findings, educational institutions may consider the following actions:



**1. Academic Performance Monitoring**

Regularly monitor student examination results and identify students who may require additional support.



**2. Study Habit Improvement**

Encourage consistent study routines and effective time management.



**3. Attendance Monitoring**

Track attendance patterns and investigate potential academic support needs.



**4. Parental Engagement**

Encourage appropriate communication between educational institutions and parents.



**5. Learning Resource Accessibility**

Review whether students have sufficient access to educational resources.



**6. Data-Driven Decision Making**

Use analytical dashboards to monitor performance indicators and support academic planning.



These recommendations should be prioritized according to the actual analytical findings.



**14. Project Folder Structure**



```text

SWYNEX-Final-Data-Analytics-Project/

│

├── 01\_Dataset/

│   └── cleaned\_student\_data.csv

│

├── 02\_SQL\_Analysis/

│   └── code\_file.sql

│

├── 03\_Python\_Analysis/

│   ├── SWYNEX\_Student\_Performance\_EDA.ipynb

│   └── EDA\_Charts/

│

├── 04\_PowerBI\_Dashboard/

│   └── Dashboard.pbix

│

├── 05\_Screenshots/

│   └── Dashboard.png

│

├── 06\_Documentation/

│

└── README.md

```



**15. Skills Demonstrated**



Through this project, the following practical skills were applied:



**Technical Skills**

\- MySQL

\- SQL querying

\- Data cleaning

\- Data validation

\- Python programming

\- Pandas

\- Matplotlib

\- Exploratory Data Analysis

\- Microsoft Power BI

\- Data visualization



**Analytical Skills**

\- Problem understanding.

\- Data interpretation.

\- Analytical thinking.

\- Identifying data patterns.

\- Business insight generation.

\- Data-driven recommendations.



**Project Skills**

\- End-to-end project development.

\- Data organization.

\- Technical documentation.

\- GitHub repository management.

\- Dashboard presentation.



**16. Project Limitations**



\- The analysis is based on the available dataset and its recorded variables.

\- Relationships identified through exploratory analysis should not be interpreted as proof of causation.

\- The analysis does not automatically represent every educational institution or student population.

\- The quality of conclusions depends on the quality and completeness of the source data.



**17. Future Enhancements**



Potential improvements include:



\- Advanced statistical analysis.

\- Correlation analysis.

\- Additional interactive Power BI reports.

\- Student performance segmentation.

\- Predictive analytics using machine learning.

\- Automated reporting and data refresh.

\- More detailed comparative analysis.



These enhancements can extend the analytical capabilities of the project.



**18. Conclusion**



The SWYNEX Final Data Analytics Project demonstrates a complete analytical workflow using real-world data analytics tools and techniques.



The project integrates data cleaning, SQL querying, Python-based exploratory analysis, and Power BI dashboard development into a unified case study.



By transforming raw student information into structured data and interactive visual reports, the project demonstrates the practical application of data analytics in the education domain.



It also highlights the importance of data quality, analytical investigation, visualization, and evidence-based decision-making.



This project represents the practical application of technical and analytical skills developed during the SWYNEX Data Analyst Internship.



\---



**Project Information**



**Project Name:** Student Performance Analytics



**Organization:** SWYNEX Technologies



**Internship Task:** Task 4 – Final Data Analytics Project



**Project Domain:** Education Analytics



**Author:** Sowmiya Balakrishnan



**GitHub Profile:** https://github.com/sowmiya19112



**Repository:** SWYNEX-Final-Data-Analytics-Project



\---



**Developed as part of the SWYNEX Data Analyst Internship.**

