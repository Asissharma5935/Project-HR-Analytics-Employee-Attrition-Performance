# HR Analytics: Employee Attrition & Performance

An employee workforce analytics project using **Power BI** and HR employee data to explore attrition, satisfaction, demographics, compensation, and tenure.

> The repository includes the Power BI report file and CSV datasets. The findings below are descriptive summaries calculated from `HR_Analytics.csv`; they should be checked against the Power BI report after refreshing the data model.

## Project Contents

| File | Purpose |
|---|---|
| `power bi final assignment.pbix` | Power BI report/dashboard |
| `HR_Analytics.csv` | HR analytics dataset used for employee attrition analysis |
| `HR_Project_Power BI.csv` | Alternative/source dataset version in a more compact column layout |
| `README.md` | Project summary, data notes, and setup instructions |

## Business Objectives

- Understand employee attrition patterns.
- Compare attrition across departments, roles, and employee characteristics.
- Explore employee satisfaction, overtime, work-life balance, and tenure.
- Review compensation and workforce demographics to support HR discussions.

## Dataset

The main `HR_Analytics.csv` file has **1,480 rows and 38 columns** in the repository snapshot. It contains employee identifiers, age group, attrition status, department, role, satisfaction indicators, monthly income, overtime status, tenure, and other HR attributes.

A structural check found 1,470 distinct `EmpID` values and 1,470 distinct `EmployeeNumber` values, so there are repeated identifier values in the file. Investigate these before treating every row as a unique employee. The second CSV appears to use a different column layout; verify which file is connected to the Power BI model before refreshing the dashboard.

## Initial Findings from `HR_Analytics.csv`

- **Attrition marked Yes:** 238 rows out of 1,480 (**16.1% of rows**).
- **Attrition marked No:** 1,242 rows.
- **Average age:** approximately 36.9 years.
- **Average monthly income:** approximately 6,504.99 (currency not specified in the file).
- **Average years at company:** approximately 7.0.
- The file contains 3 departments and 9 job roles.
- Attrition-Yes rows by department: Research & Development 133, Sales 93, Human Resources 12.

These are descriptive calculations from the CSV snapshot. Because employee identifiers repeat, interpret the percentages as row-based until duplicate IDs and the correct denominator are checked. These figures are not represented as verified Power BI visual outputs.

## Suggested Dashboard Sections

1. **Workforce Overview:** total employee rows, attrition count/rate, average age, average tenure.
2. **Attrition Analysis:** attrition by department, job role, age group, overtime, and tenure.
3. **Satisfaction & Work-Life Balance:** job satisfaction, environment satisfaction, relationship satisfaction, and work-life balance.
4. **Compensation & Experience:** monthly income/salary slab, job level, years at company, and years since last promotion.

Suggested slicers: Department, Job Role, Gender, Age Group, Business Travel, and OverTime.

## Tools & Skills

- Microsoft Power BI
- Power Query for data inspection and transformation
- DAX measures and calculated columns (where present in the PBIX)
- Data modeling and interactive visual analysis
- HR metrics and attrition analysis

## How to Open

1. Download `power bi final assignment.pbix`.
2. Open it in Microsoft Power BI Desktop.
3. Review the data source settings and confirm which CSV is used.
4. Refresh the model after checking the data types and employee ID duplicates.
5. Compare report visuals with the initial CSV findings above.

## Data Quality Checks Recommended

- Investigate repeated `EmpID` and `EmployeeNumber` values in `HR_Analytics.csv`.
- Decide which CSV version is the intended source for the PBIX and document that choice.
- Confirm the attrition denominator before publishing a definitive attrition rate.
- Check for blank values, data types, and category consistency in Power Query.

## Author

**Asish Kumar Sharma**

## Repository

[View this project on GitHub](https://github.com/Asissharma5935/Project-HR-Analytics-Employee-Attrition-Performance)
