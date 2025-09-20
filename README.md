# Diabetes_Expenditures
Analyzing and visualizing expenditures directly attributable to Diabetes in the US from 2019-2023 

## Data:

All Data was sourced from [MEPS](https://meps.ahrq.gov/data_stats/download_data_files.jsp), 8 files were used across all 5 years:
- [Medical Conditions](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=1%2CHousehold+Full+Year+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Medical+Conditions)
- [Prescriptions](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Prescribed+Medicines)
- [Event Link](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Appendix+to+MEPS)
- [Outpatient Visits](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Outpatient+Visits)
- [Inpatient Stays](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Hospital+Inpatient+Stays)
- [ER Visits](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Emergency+Room+Visits)
- [Office Visits](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Office-Based+Medical+Provider+Visits)
- [Home health](https://meps.ahrq.gov/data_stats/download_data_files_results.jsp?cboDataYear=All&cboDataTypeY=2%2CHousehold+Event+File&buttonYearandDataType=Search&cboPufNumber=All&SearchTitle=Home+Health)

## Preprocessing

- Data was loaded and transformed in Python using pandas.
- Diabetes related conditions were filtered based on ICD10CM code E11 and these conditions were linked to all event datasets using the eventlink file.
- Yearly files were merged into a single table and person level weights were applied to expenditures to ensure nationall representative values.

## Visualization - IN progress

- [x] Total number of treated patients per year
- [x] Expenses by payer and event type
- [x] Average payment per person per event type 
- [ ] Expenses by prescription type
- [ ] percent change since selected year
- [ ] adjust values for inflation

