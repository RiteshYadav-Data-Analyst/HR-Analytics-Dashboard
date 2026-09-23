# HR Analytics Dashboard

## Project Overview

This project is an HR Analytics Dashboard created using Power BI.

The main purpose of this dashboard is to analyze employee attrition and understand employee-related patterns across different departments, age groups, salary slabs, education fields, job roles, and years at the company.

The dashboard is interactive and allows users to filter the analysis using Gender and Department.

## Tools Used

- Power BI
- Power Query
- DAX
- Microsoft Excel

## Key KPIs

The dashboard contains the following six KPIs:

- Total Employee Count
- Attrition Rate
- Attrition Count
- Average Employee Age
- Average Salary
- Average Years at Company

## Dashboard Visualizations

The dashboard includes:

- Donut Chart – Attrition Rate by Education Field
- Clustered Column Chart – Attrition by Age Group
- Horizontal Bar Chart – Attrition by Salary Slab
- Matrix – Job Role vs Job Satisfaction Level
- Line Chart – Years at Company vs Attrition Count
- Column Chart – Department vs Number of Employees Left

## Filters

The dashboard includes two slicers:

- Gender
- Department

These slicers make the dashboard interactive and allow users to analyze employee attrition based on selected categories.

## Data Preparation

I used Power Query to prepare the HR data before creating the dashboard.

The main data preparation steps included:

- Checking data types
- Checking null values
- Checking duplicate records
- Removing unnecessary columns
- Renaming columns where required
- Applying the required transformations

## DAX Measures

### Total Employees

Total Employees = COUNT('HR Data'[EmployeeNumber])

### Total Attrition

Total Attrition =
CALCULATE(
    COUNT('HR Data'[EmployeeNumber]),
    'HR Data'[Attrition] = "Yes"
)

### Attrition Rate

Attrition Rate =
DIVIDE(
    [Total Attrition],
    [Total Employees],
    0
)

### Average Employee Age

Average Employee Age =
AVERAGE('HR Data'[Age])

### Average Salary

Average Salary =
AVERAGE('HR Data'[MonthlyIncome])

### Average Years at Company

Average Years =
AVERAGE('HR Data'[YearsAtCompany])

## Key Insights

The dashboard helps identify:

- Overall employee attrition
- Attrition patterns across age groups
- Departments with higher employee exits
- Attrition across different salary slabs
- Attrition patterns across education fields
- Relationship between job roles and job satisfaction
- Attrition count based on years at the company

## Conclusion

This dashboard provides an interactive view of employee attrition and workforce patterns.

It can help HR teams understand where employee attrition is higher and identify areas that may require further investigation.
