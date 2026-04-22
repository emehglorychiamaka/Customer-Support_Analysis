# Customer-Support_Analysis
Customer Support Performance Analysis using SQL, Power BI &amp; Data Storytelling

## Project Overview
This project analyzes customer support operations to uncover performance gaps, improve resolution efficiency, and enhance customer satisfaction. Using SQL and Power BI, the analysis provides actionable insights into how support teams handle cases across different dimensions.

## Problem Statement
Customer support teams often struggle with:
- Low resolution rates  
- High escalation levels  
- Inefficient handling time  
- Inconsistent performance across vendors and channels  

This project aims to identify these inefficiencies and provide data-driven insights for improvement.

##  Methodology
The analysis was carried out in two key stages:

### 1. Data Preparation (SQL)
- Extracted and cleaned data from multiple tables  
- Joined datasets to create a unified view of support cases  
- Calculated key performance metrics  

### 2. Data Visualization (Power BI)
- Built an interactive dashboard  
- Tracked KPIs such as:
  - Resolution Rate  
  - Escalation Rate  
  - First Contact Resolution (FCR)  
  - Average Handling Time  

##  Data Integration (Joins)
To enable meaningful analysis, multiple tables were combined to create a complete dataset.

## Why Join Tables?
- To connect case data with support attributes  
- To enable multi-dimensional analysis (vendor, location, support type)  
- To improve accuracy of performance metrics  

### SQL Join
--5  CREATE JOINED DATA SET --
CREATE VIEW joined_table AS
SELECT
    s.CASE_ID,
    s.SURVEY_SOLVED_ISSUE,
    s.SURVEY_DATE_SENT,

    c.CASE_CREATION_DATE,
    c.CASE_FIRST_OUTSOURCE_VENDOR_NAME,
    c.CASE_CS_FIRST_OFFICE_LOCATION,
    c.CASE_CS_FIRST_EMPLOYEE_IS_NEWBIE,
    c.CASE_CS_FIRST_EMPLOYEE_SUPPORT_TYPE,
    c.CASE_HAS_QUICK_REPLY,
    c.CASE_IS_FCR,
    c.CASE_CONTACT_COUNT,
    c.CASE_END_TO_END_RESOLUTION_TIME_MINUTES,
    c.CASE_TOTAL_HANDLING_TIME_MINUTES,
    c.CASE_TOTAL_NET_HANDLING_TIME_MINUTES,
    c.CASE_HAS_ESCALATION,
    c.CASE_HAS_L2_OR_NATIVE_ESCALATION,
    c.CASE_HAS_NON_CS_ESCALATION

FROM Survey_table s
JOIN Case_table c
ON s.CASE_ID = c.CASE_ID;

## Key Insights
- Resolution rate: 54.8%
- Escalation rate: 19.8%
- FCR significantly reduces handling time
- Vendor and support type impact performance

## Files Included
- SQL queries
- Power BI dashboard
- Presentation slides

## Author
Emeh Glory Chiamaka 
