# Average_Junior_DA_Annual_Income
An exploratory data analysis of junior Data Analyst salaries in Canada and the United States, normalized to CAD. This project focuses on market distribution, median vs. average comparisons, and early-career salary progression to establish realistic compensation expectations beyond simple summary statistics.


################## 'Average Junior DA Annual Income' ##################

Objective/Goal
The objective of this analysis is to assess how junior data analyst compensation compares to the regional living wage in my region. By grounding salary expectations in wage data, this project supports a justified target compensation range rather than arbitrary market figures.

STEPS TAKEN
~	Find The Average Annual Income of Junior DA.
~	Clean & Validate Data
~	Analyze, Review Data
~	Look For Trends Patterns
Build Visualization and Narrative To Present Findings

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -


SQL

/*
Project Title:
Average Junior Data Analyst Income vs Regional Cost of Living

Author:
Warren Perry

Date:
2026-01-17

Description:
This analysis examines reported junior data analyst compensation 
to understand market alignment and compensation expectations.

Data Sources:
- Dataset: jobs_in_data.csv
- Source: Kaggle
- URL: https://www.kaggle.com/datasets/hummaamqaasim/jobs-in-data
- Currency: CAD (converted where applicable)

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
  
SELECT
employee_residence,
job_title,
work_year,
salary,
salary_currency
FROM
`da-income-compared-to-rcol.jobs_in_data.Jobs`
WHERE
job_title = 'Data Analyst'
AND employee_residence 
IN ('Canada', 'United States')
AND experience_level IN ('Entry-level', 'Mid-level')
ORDER BY work_year;

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

Excel Formulas

USD Conversion To CAD
=IF(E2="USD",D2*$J$2,D2)
Salary Median
=MEDIAN(F2:F395)
Salary Average
=AVERAGE(F2:F395)

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

Junior Data Analyst Salaries: Market vs. Summary Averages (CAD)

This analysis examines junior Data Analyst salaries in Canada and the United States, converted to CAD, to better understand realistic compensation relative to market distribution rather than relying on limited or self-reported averages. The visualization shows a wide salary spread, with a dense early-career cluster below the overall average and a clear upward trend as experience increases, highlighting how mean values can overstate typical entry-level earnings. By comparing individual salary observations against median and average reference lines, the data supports a justified target compensation range rather than an arbitrary benchmark, demonstrating that salaries in the $90,000–$100,000 CAD range fall within observed market outcomes and are attainable as analysts progress beyond initial entry-level roles.

 
File Download Links




