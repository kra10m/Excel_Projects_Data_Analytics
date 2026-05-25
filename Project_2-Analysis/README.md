# Excel Salary Analysis Project

## Introduction

This project was created to explore the relationship between salaries, skills, and job demand in the data science job market. Using real-world job posting data, the analysis focuses on identifying high-paying skills, salary differences across regions, and the most in-demand technologies for data professionals.

### Analysis File

My final analysis workbook is in [`Project_2_Analysis.xlsx`](Project_2_Analysis.xlsx).

## Excel Skills Used

The following Excel skills were used in this project:

* Pivot Tables.
* Pivot Charts.
* DAX (Data Analysis Expressions).
* Power Query.
* Power Pivot.

## Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. It includes details on:

* Job titles.
* Salaries.
* Locations.
* Skills.

## Analysis Questions

The project focused on answering the following questions:

1. Do more skills lead to higher pay?
2. What are the salary differences across regions?
3. What are the most common skills for data professionals?
4. What is the pay for the top 10 skills?

## Analysis Build

### Power Query

#### Data Extraction and Cleaning

Power Query was used to extract and transform the original dataset. Two separate queries were created:

* A table containing all job posting information.
* A table listing skills associated with each job ID.

The data was then cleaned by:

* Changing column data types.
* Removing unnecessary columns.
* Cleaning and trimming text values.
* Preparing the dataset for analysis.

### Power Pivot

#### Data Model Creation

Power Pivot was used to create a data model by connecting the jobs table and skills table using the `job_id` column. This relationship allowed for more advanced analysis using PivotTables and DAX measures.

### Pivot Tables and DAX

#### Median Salary Analysis

PivotTables were used to summarize salary data by job title and region. DAX measures were created to calculate median salaries.

```excel
Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
```

A separate DAX measure was also created to calculate median salary specifically for jobs in the United States.

```excel
=CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States"
)
```

### Pivot Charts

#### Salary and Skill Comparison

A combo PivotChart was created to compare:

* Median salary by skill.
* Skill likelihood percentage.

The chart used:

* Clustered columns for salary values.
* A line chart with markers for skill likelihood percentages.

This visualization helped identify which skills are both highly demanded and associated with higher salaries.

## Key Insights

### Skills and Salary Relationship

The analysis showed a positive relationship between the number of required skills and salary levels. Roles such as Senior Data Engineer and Data Scientist typically offered higher salaries and required broader technical skill sets.

### Regional Salary Differences

Data-related jobs in the United States generally showed higher median salaries compared to non-US regions, especially for senior and technical roles.

### Most In-Demand Skills

SQL and Python appeared as the most commonly requested skills across data jobs. Cloud-related technologies such as AWS and Azure were also highly represented.

### Top Paying Skills

Skills like Python, SQL, and Oracle were associated with higher median salaries, while general office tools such as Word and PowerPoint were linked to lower salary ranges.

## Conclusion

This project demonstrates how Excel can be used for advanced data analysis using tools such as Power Query, Power Pivot, PivotTables, DAX, and charts. The analysis highlights the importance of technical and specialized skills in securing higher-paying data roles and provides valuable insights into salary trends and skill demand across the data job market.
