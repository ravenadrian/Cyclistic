# Cyclistic
Coursera Google Data Analytics Capstone Project

### Project Objective
As a junior analyst at a fictional bike-share company in Chicago (Cyclistic) I am being tasked to assist the marketing analysts by assessing their data to solve one of 3 current issues:
- How do annual members and casual riders use Cyclistic bikes differently?

I will be using data from (12 months of ridership logs - July 2022-June 2023 provided by Motivate International [license](link)

The tools I will use to analyze data and present my findings will be BigQuery by Google (SQL), Tableau, GitHub, and Google Slides.


I will be utilizing the 6-step procedure outlined in the Google Data Analytics method: *Ask, Prepare, Process, Analyze, Share, Act*

## ASK
In this step we consider our stakeholders and clearly define the business task.
The stakeholders here include Cyclistic executives, and, more acutely, the marketing analyst team and Lily Moreno (Marketing Manager). She has delivered a very direct task which was defined in the objective: Find all ways that annual member activity differs from casual rider activty, relevant to finding ways to covert casual members through marketing tactics.

## PREPARE
In this step we cobmine the individual files and then confirm the consistency and accuracy of the data and its formatting to prepare for processing.
To combine data into one table I used the ``UNION`` function as shown:
```
CREATE TABLE `jul23_jun24_cyclistic.combined_cyclistic` AS (
  SELECT * FROM `jul23_jun24_cyclistic.01_24_cyclistic`
  UNION ALL
  SELECT * FROM `jul23_jun24_cyclistic.02_24_cyclistic`
  UNION ALL
  SELECT * FROM `jul23_jun24_cyclistic.03_24_cyclistic`
  UNION ALL
  SELECT * FROM `jul23_jun24_cyclistic.04_24_cyclistic`
  UNION ALL
  SELECT * FROM `jul23_jun24_cyclistic.05_24_cyclistic`
  UNION ALL
  SELECT * FROM `jul23_jun24_cyclistic.06_23_cyclistic`
  UNION ALL
  SELECT * FROM `jul23_jun24_cyclistic.07_23_cyclistic`
  UNION ALL
  SELECT * FROM `jul23_jun24_cyclistic.08_23_cyclistic`
  UNION ALL
  SELECT * FROM `jul23_jun24_cyclistic.09_23_cyclistic`
  UNION ALL
  SELECT * FROM `jul23_jun24_cyclistic.10_23_cyclistic`
  UNION ALL
  SELECT * FROM `jul23_jun24_cyclistic.11_23_cyclistic`
  UNION ALL
  SELECT * FROM `jul23_jun24_cyclistic.12_23_cyclistic`
);
```

Exploratory Stage - getting familiar with my the data.
- Overall, what is the total member rides vs casual rides compared to % of each segment
- Can we add zip codes to our data to define rides by geographic location?
- How do average ride times for members
- Do members and casual riders use assist-style bikes more?
- How does ridership change by month of the year and weekdays/weekends by segment?
  
Data Anomalies/Patterns to check for
- null vallues
- min and max ride time
- check for duplicate rows
- check attribute lengths for consistency

Unaswerable Questions (but questions I would like to ask my stakeholders for further clarity)
- how do prices differ for each segment
- Why do 

## PROCESS
1. Combine Data into one table

  
3. Clean data

4. Staion names - public rack remove

```SELECT SDIIOKPF```


## ANALYZE

## SHARE

## ACT
