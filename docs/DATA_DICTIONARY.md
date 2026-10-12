# HR Analytics Dataset Guide

This guide describes the fields visible in the CSV headers in this repository. Column descriptions are based on field names and typical HR usage; validate them against the dataset documentation and the transformations in the Power BI file before using them for formal reporting.

## Employee Identification
- `EmpID`, `EmployeeNumber`: employee identifier fields. The main `HR_Analytics.csv` file contains repeated values; check duplicates before counting unique employees.
- `EmployeeCount`, `Over18`, `StandardHours`: fields that may be constant or legacy fields; confirm whether they add analytical value.

## Demographics
- `Age`, `AgeGroup`, `Gender`, `MaritalStatus`, `Education`, `EducationField`: employee profile attributes.

## Job and Organization
- `Department`, `JobRole`, `JobLevel`, `BusinessTravel`, `DailyRate`, `HourlyRate`, `MonthlyRate`, `MonthlyIncome`, `SalarySlab`: role, organization, travel, and compensation-related fields.
- `NumCompaniesWorked`, `TotalWorkingYears`, `YearsAtCompany`, `YearsInCurrentRole`, `YearsWithCurrManager`, `YearsSinceLastPromotion`: work experience and tenure indicators.

## Attrition and Employee Experience
- `Attrition`: indicates whether the row is marked as attrition Yes/No in the dataset.
- `OverTime`: overtime category.
- `EnvironmentSatisfaction`, `JobSatisfaction`, `JobInvolvement`, `RelationshipSatisfaction`, `WorkLifeBalance`: employee experience ratings.
- `StockOptionLevel`, `PercentSalaryHike`, `PerformanceRating`, `TrainingTimesLastYear`, `DistanceFromHome`: other employment and performance-related fields.

## Data Quality Checklist

1. Compare row count with distinct `EmpID` and `EmployeeNumber` counts.
2. Inspect missing values in key dimensions and numeric metrics.
3. Verify whether ratings are stored as numeric ordinal scales and document the label mapping used in Power BI.
4. Confirm the meaning and units of compensation fields before labeling currency.
5. Confirm which CSV version is loaded into the PBIX. `HR_Analytics.csv` and `HR_Project_Power BI.csv` have different layouts, so measures may require different field mappings.
6. Validate attrition rate denominator; do not calculate it from row count if multiple rows may represent the same employee.
