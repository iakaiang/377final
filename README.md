##  INST414-Final

This project analyzes COVID-19 in the United States from March 1, 2020 until December 1, 2022. The first was an analysis the accuracy of three distinct COVID-19 data sources (health department, county, and state), in order to see if discrepancies existed in the reporting and/or recording of cases and deaths. Secondly, COVID-19 cases in DMV Area were each compared to their respective population percentages being tested, in order to consider any correlations that may have existed between the two factors. 

The DMV were chosen for this study. Because it is where students in UMD will most likely to visit. So it's important to have a collective measures to contain COVID-19 within this region. The comparison of DMV area allows an examination into the effectiveness of certain mandates on containing COVID-19 spread.
 
## Data Sources ##
* https://covidtracking.com/data/download
* https://www.kaggle.com/fireballbyedimyrnmom/us-counties-covid-19-dataset?select=us-counties.csv
* https://raw.githubusercontent.com/nytimes/covid-19-data/master/us-states.csvcovid19-us-county-jhu-data-demographics/data?select=us_county.csv
* https://www.cdc.gov/covid-data-tracker/#cases


State Statistics:
* Maryland was ranked second highest in total positive case counts for all US states. Maryland's cases started to increase over 1,000 per day on 1/1/22. Virginia was ranked highest in DMV Area. The largest positive cases period is similar to Marylands. And DC has the least positive cases also the least tested state.
---

## Process ##

Data was initially extracted from the from the health department, county, and state in the form of CSV files. The CSV files were then loaded into Python as Pandas DataFrames via Jupyter Notebook. Data cleanup was performed to remove null values, filter for the time frame and three states being studied, and format column names and data types to be synonymous for all 3 sources. Statistical analysis was then performed using NumPy and SciPy, and Matplotlib was used to create visualizations.

---

## Analysis & Conclusions ##
### How did the three data sets compare and did they reveal consistencies or inconsistencies:
* A line plot was produced using each of the three different data sources. The line plots examine date versus total Covid-19 cases in the 3 states. The line plots were compared to see if there were any descrepancies in the data.
* The three data sets selected for this analysis proved to be staistically significantly similar. The histogram showed the data sets overlayed each other indicating the data sets are similar. For further analysis, a t-test was performed. This resulted in t-scores with p-values larger than .05, therefore, the difference found is not statistically significanlty different.

### What percentage of the population was tested and how much did testing vary from state to state? Did the testing percentages correlate to COVID-19 count?:
* The percentage of each states population that was tested over time was plotted and then compared. Additionally, a linear regression was performed to see if the average testing percentage of each state correlates to the average daily COVID-19 count.
* The correlation coefficient between testing percentages and COVID-19 count was only 0.13, which indicates there is no relationship between the two variables. This is also demonstrated in the scatter plot where the data points are spread all over rather than being clustered in a linear fashion. The r-squared value of 0.0136 indicates that only 0.96% of the movements of daily COVID-19 count (dependent variable) are explained by the movements in the testing percentage (independent variable). Thus, there is no relationship between the two at all. 
