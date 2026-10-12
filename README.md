# HR Analytics: Employee Attrition & Performance

![Power BI](https://img.shields.io/badge/Tool-Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black) ![HR Analytics](https://img.shields.io/badge/Focus-HR_Analytics-5A4FCF?style=for-the-badge)

An employee workforce analytics project built around **Power BI** and HR data. It explores employee attrition, satisfaction, demographics, compensation, overtime, and tenure.

## Repository Structure

```text
.
├── data/
│   ├── HR_Analytics.csv
│   └── HR_Project_Power_BI.csv
├── powerbi/
│   └── HR_Analytics_Employee_Attrition.pbix
├── docs/
│   └── DATA_DICTIONARY.md
└── README.md
```

## Project Objectives

- Explore employee attrition patterns across departments and job roles.
- Compare attrition with employee demographics, overtime, satisfaction, and tenure.
- Review compensation and workforce characteristics.
- Present HR metrics in an interactive Power BI report to support further investigation.

## Files

| File | Description |
|---|---|
| `powerbi/HR_Analytics_Employee_Attrition.pbix` | Power BI report file |
| `data/HR_Analytics.csv` | HR dataset with age group, employee ID, attrition, department, satisfaction, income, and tenure fields |
| `data/HR_Project_Power_BI.csv` | A second CSV version with a different column layout |
| `docs/DATA_DICTIONARY.md` | Field groups and data-quality notes |

## Dataset Summary

A structural check of `data/HR_Analytics.csv` found **1,480 data rows and 38 columns**. The file contains 1,470 distinct values in `EmpID` and 1,470 distinct values in `EmployeeNumber`. This means identifiers repeat in the file and should be investigated before treating every row as a unique employee.

Initial row-level summaries from `HR_Analytics.csv`:
- Attrition = Yes: 238 rows (16.1% of the 1,480 rows).
- Attrition = No: 1,242 rows.
- Average age: approximately 36.9 years.
- Average monthly income: approximately 6,504.99 (currency is not specified in the file).
- Average years at company: approximately 7.0.
- Attrition = Yes rows by department: Research & Development 133, Sales 93, Human Resources 12.

These are calculated from the CSV snapshot, not verified dashboard outputs. Because employee identifiers repeat, treat rates above as **row-based** until duplicates and the correct denominator are resolved. The second CSV has a different schema, so confirm which dataset is connected to the PBIX before refreshing visuals.

## Suggested Dashboard Areas

1. **Workforce Overview:** employee count, attrition count/rate, average age, and average tenure.
2. **Attrition Analysis:** attrition by department, job role, age group, overtime, and tenure.
3. **Satisfaction & Work-Life Balance:** job, environment, and relationship satisfaction plus work-life balance.
4. **Compensation & Experience:** monthly income, salary slab, job level, years at company, and years since promotion.

Possible slicers include Department, Job Role, Gender, Age Group, Business Travel, and OverTime.

## Tools and Skills

- Microsoft Power BI
- Power Query data inspection and transformation
- DAX measures and calculated columns (where implemented in the report)
- Data modeling and interactive visual analysis
- HR metrics and attrition analysis

## How to Open the Report

1. Download `powerbi/HR_Analytics_Employee_Attrition.pbix`.
2. Open it using Power BI Desktop.
3. Review the data source settings and identify which CSV is connected.
4. Check employee ID duplicates, blank values, data types, and category consistency in Power Query.
5. Refresh the report and compare its visuals with the source data.

## Data Quality Checks Before Sharing Results

- Investigate repeated `EmpID` and `EmployeeNumber` values in the main CSV.
- Decide which CSV is the authoritative source for the PBIX and document it.
- Confirm the denominator used for attrition rate.
- Check nulls, data types, and category consistency before publishing final insights.

## Author

**Asish Kumar Sharma**
