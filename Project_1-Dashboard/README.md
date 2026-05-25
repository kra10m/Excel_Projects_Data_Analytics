# Excel Salary Dashboard

## Introduction

This salary dashboard was created to help job seekers explore compensation across data-related roles and make better career decisions. It uses real-world job data and presents insights on job titles, salaries, locations, and skills in a clear dashboard format.

### Dashboard File

My final dashboard is in [`Salary_Dashboard.xlsx`](Salary_Dashboard.xlsx).

## Excel Skills Used

The following Excel skills were used in this project:

- Charts.
- Formulas and functions.
- Data validation.

## Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. It includes details on:

- Job titles.
- Salaries.
- Locations.
- Skills.

## Dashboard Build

### Charts

#### Data Science Job Salaries

A horizontal bar chart was used to compare median salaries across job titles. The chart is sorted by salary in descending order to improve readability and highlight higher-paying roles.

#### Country Median Salaries

A map chart was used to visualize median salaries by country. This makes it easy to spot geographic salary differences and compare regions at a glance.

### Formulas and Functions

#### Median Salary by Job Title

```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

This formula calculates the median salary based on job title, country, and schedule type while excluding blank salary values.

#### Count of Job Schedule Type

```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

This formula creates a filtered list of valid job schedule types by removing entries containing “and,” commas, or zero values.

### Data Validation

A filtered list was used for data validation in the Job Title, Country, and Type fields. This helps keep inputs consistent and improves the usability of the dashboard.

## Conclusion

This dashboard shows how Excel can be used to analyze salary trends across different data-related roles. It helps users understand how location and job type influence salaries and supports better career decisions.
