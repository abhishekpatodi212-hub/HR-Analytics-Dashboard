# HR-Analytics-Dashboard

# HR Analytics Dashboard
**Stack:** Excel + Power BI

## Overview
1,500-employee HR dataset covering demographics, tenure, satisfaction, performance,
and attrition — the kind of dataset an HR analytics team uses to understand *why*
people leave.

## Files
| File | Purpose |
|---|---|
| `hr_data.csv` | Raw dataset (1,500 rows, 12 columns) |
| `HR_Analytics_Dashboard.xlsx` | Excel dashboard: Raw Data table, formula-driven Summary sheet (headcount/attrition by department, satisfaction, overtime, gender split), Charts sheet |

This project intentionally skips a separate SQL layer since the recruiter-facing
brief lists it as **Excel + Power BI** — the Excel workbook itself is the
analysis layer here, with live formulas so it recalculates if data changes.

## Key columns
`EmployeeID, Department, Gender, Age, TenureYears, AnnualSalary, SatisfactionScore, PerformanceRating, OverTime, WorkFromHome, Education, Attrition`

## Power BI dashboard design
1. **Workforce Overview** — headcount by department, gender split, education mix.
2. **Attrition Drivers** — attrition rate by department, satisfaction score, and overtime status side by side, so the biggest lever is obvious at a glance.
3. **Compensation** — average salary by department vs performance rating, to check pay-for-performance alignment.

Import `hr_data.csv` directly into Power BI; the Excel Summary tables mirror the
aggregations each visual would need.

## Key insights (from this synthetic dataset)
- Employees who work overtime churn at a clearly higher rate than those who don't — a workload/burnout signal worth investigating.
- Attrition is heavily concentrated among employees who rate satisfaction 1–2 out of 5 — satisfaction score is the strongest single predictor here.
- Attrition skews toward early-tenure employees, again pointing at onboarding and first-year experience as the highest-leverage fix.
