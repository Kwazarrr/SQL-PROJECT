# COVID-19 Data Exploration Using SQL

## Project Overview

This project explores COVID-19 data using Microsoft SQL Server (T-SQL). The goal is to practice data exploration, aggregation, joins, and analytical SQL techniques while examining reported COVID-19 cases, deaths, and vaccination activity.

The repository contains SQL queries and two Excel datasets.

## Datasets

**CovidDeaths.xlsx**

Contains COVID-19 case and death statistics, including:
- Country or location
- Continent
- Date
- Population
- Total and new cases
- Total and new deaths

**CovidVaccinations.xlsx**

Contains vaccination-related data, including daily vaccination counts used in the SQL analysis.

## Project Objectives

- Explore reported COVID-19 cases and deaths.
- Compare case counts relative to population.
- Identify countries with the highest reported cumulative case and death counts.
- Estimate cumulative deaths by continent using country-level aggregations.
- Explore global reported cases and deaths.
- Join COVID-19 death and vaccination datasets.
- Calculate running totals of reported vaccination doses.

## SQL Skills Demonstrated

- **SELECT, WHERE, ORDER BY** — data selection and filtering
- **GROUP BY, SUM, MAX** — data aggregation
- **JOIN** — combining datasets
- **CTEs (Common Table Expressions)** — structuring analytical queries
- **Window Functions** — calculating running totals using `SUM() OVER()`
- **Temporary Tables** — storing intermediate results
- **Views** — creating reusable queries
- **CAST and CONVERT** — data type conversion

## Analysis Performed

### 1. Cases and Deaths

Explored reported COVID-19 cases and deaths and calculated ratios between cumulative reported deaths and cases.

### 2. Cases Relative to Population

Compared cumulative case counts with population figures to examine reported case prevalence across locations.

### 3. Country and Continent Comparisons

Used aggregate functions to compare countries and estimate total deaths by continent from country-level cumulative counts.

### 4. Global Statistics

Aggregated reported new cases and deaths to calculate overall totals and a reported case-fatality ratio.

### 5. Vaccination Activity

Joined case and vaccination datasets by location and date. Used window functions, CTEs, and temporary tables to calculate and organize cumulative vaccination counts.

Vaccination dose counts should not be interpreted as counts of unique vaccinated individuals.

## Technologies

- Microsoft SQL Server (T-SQL)
- SQL Server Management Studio (SSMS) or another compatible SQL Server client
- Microsoft Excel (source datasets)

## How to Run

1. Download the repository files.
2. Create a database named `PortfolioProject` in SQL Server.
3. Import `CovidDeaths.xlsx` and `CovidVaccinations.xlsx` into tables named `CovidDeaths` and `CovidVaccinations`.
4. Verify column names, data types, and missing values after importing.
5. Open `COVID Portfolio Project.sql` in your SQL editor.
6. Execute and inspect individual analysis sections.

Some queries create temporary tables or a view and may require appropriate database permissions.

## Limitations

- The source publication and snapshot date of the included datasets are not documented.
- Missing values, reporting differences, and revisions may affect results.
- Continental totals based on country-level maximum cumulative values are approximate and may combine observations from different dates.
- Case and death ratios do not represent an individual's probability of dying from COVID-19.
- The SQL queries are portfolio exercises; the complete script has not yet been independently validated against the imported datasets.
