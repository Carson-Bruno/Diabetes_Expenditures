# Diabetes_Expenditures
Analyzing and visualizing expenditures directly attributable to Diabetes in the US from 2019-2023 

[Tableau Dashboard](https://public.tableau.com/app/profile/carson.bruno/viz/diabetes_expenditure_dashboard/Dashboard1)
## Data:

All Data was sourced from [MEPS](https://meps.ahrq.gov/data_stats/download_data_files.jsp), 9 files were used across all 5 years:
- [Medical Conditions](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=1%2CHousehold+Full+Year+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Medical+Conditions)
- [Prescriptions](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Prescribed+Medicines)
- [Event Link](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Appendix+to+MEPS)
- [Outpatient Visits](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Outpatient+Visits)
- [Inpatient Stays](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Hospital+Inpatient+Stays)
- [ER Visits](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Emergency+Room+Visits)
- [Office Visits](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Office-Based+Medical+Provider+Visits)
- [Home health](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Home+Health)
- [Full Year Files](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=1%2CHousehold+Full+Year+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Consolidated+Data)

## Preprocessing

- Data was loaded and transformed in Python using pandas.
- Diabetes related conditions were filtered based on ICD-10-CM code E11 and these conditions were linked to all event datasets using the eventlink file.
- Yearly files were merged into a single table and person level weights were applied to expenditures to ensure nationaly representative values.

## Questions

- How have total expenditures changed in the 5 year period
- What is the distribution of expenses by payer and event type
- What factors are driving potential increases in expenses
- what specific medications contribute most to rising costs
![screen](https://github.com/Carson-Bruno/Diabetes_Expenditures/blob/main/complete_dashboard.png)

## Insights
- The economic toll that expenditures attributable to diabetes has continues to increase, accounting for 23.24% of total US healthcare expenses in 2023 (an 81.16% increase since 2019)
- Increases in total expenses are largely driven by a rise in the total number of people recieving treatment each year. Further analysis could break this down by diabetes type and health or demographic factors that may be contributing to the rising prevalence of diagnosed cases.  
- Prescription spending via Medicare routinely accounts for the highest percentage of expenditures.
- The growing increase in spending on prescriptions is largely led by increases in both the amount of Noninsulin glucose lowering medicines prescribed (22,576,735 in 2023, +19% since 2019) as well as the average cost of these medicines ($3,590 in 2023, +93.41% since 2019).
