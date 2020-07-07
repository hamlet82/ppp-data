# PPP Data

Data from and analysis of the Paycheck Protection Program, from the US Treasury Department.

[Originals downloadable here.](https://home.treasury.gov/policy-issues/cares-act/assistance-for-small-businesses/sba-paycheck-protection-program-loan-level-data)

original-files includes all of the .csv files from each of the state and territory folders, which includes all loans less than $150K. The csv file for loans over $150K was too large to share here without git lfs, so I split the file into two parts, a and b. Both have the same header row.

combined-files contains concatenated versions of all data, at both loan levels. Because the columns contained for $150K+ loans differ from those for loans under $150K, I've modified the data thus:

- Added a LoanMin and LoanMax column. For $150K+ loans, which are reported as a range, the lower end of the range is given as LoanMin, the upper end as LoanMax. For loans under $150K, the LoanAmount is reported as both LoanMin and LoanMax.
- Inserted empty values for Business and Address for loans under $150K, for which that data was not reported.

There may be other errors present from my transformations.
Refer to Treasury's initial files for the best versions of the data.
Other errors in the data come directly from Treasury.
