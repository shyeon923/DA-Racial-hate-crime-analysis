# Analyzing Racial Hate Crimes in the United States

*Last Updated*: Nov. 15. 2022

*Author*: Seung Hyeon Mandy Hong

*Denison University, Fall 2022, DA 401 Senior Research*

# Description
A crime where offenders' bias against race/ethnicity/ancestry acts as a primary motivation is defined as a racial hate crime (United States Department of Justice, n.d.). In 2020, hate crime in the US hit a historic high in 12 years (Carrega & Krishnakumar, 2021). Among 7,554 incidents, 61.9% were racial hate crimes, and among those racial hate crimes, two racial groups, Black or African American and Asian, had the highest increase (146% and 173% each) (Federal Bureau of Investigation, 2021). While most of the recent hate crimes involved a racial bias, past studies included all categories of hate crimes rather than focusing on racial hate crimes . Our research focuses on all racial hate crimes, and racial hate crimes involving African American or Black and Asian victims. We are primarily interested in answering three questions; (a) What is the trend of racial hate crimes over time? (b) What demographic and socioeconomic variables contribute to racial hate crimes? (c) What supervised model can best predict racial hate crimes? To answer (a), we use time series analysis. To answer (b) and (c), we use stepwise multiple regression and *k* nearest neighbors algorithm.

# Software
I used *Python 3* to collect and clean data (Van Rossum & Drake, 2009). For descriptive and predictive analysis, I used R v4.1.3 (R Core Team, 2022). Five packages were also used: *caret* (*v6.0-91*; Kuhn, 2022), *ggplot2* (Wickham, 2016), *astsa* (*v1.16*; Stoffer & Poison, 2022), *xts* (*v0.12.1*; Ryan & Ulrich, 2020), and *car* (Fox & Weisberg, 2019) packages.

# Data
Main datasets come from the Federal Bureau of Investigation Crime Data Explorer (***hate_crime.csv***) and U.S Census Bureau (***CENSUS.DA.csv***). As a result of cleaning data, we have 12 additional data sets listed below.

**Time series data for racial hate crimes** (3 columns with 360 rows, monthly from 1991 to 2020)
1. *all_race_hc_ts.csv*: three columns are year, month, and number of all racial hate crimes
2. *black_hc_ts.csv*: three columns are year, month, and number of anti-Black hate crimes
3. *asian_hc_ts.csv*: three columns are year, month, and number of anti-Asian hate crimes

**Hate crime data by states from 2016 to 2020** (260 rows)

4. *state_hc.csv*: two columns are state and sum of number of all racial hate crimes from 2016 to 2020 by states
5. *state_hc_five_years.csv*: three columns are state, year, and number of all racial hate crimes reported each year by states 
6. *black_state_hc.csv*: two columns are state and sum of number of anti-Black hate crimes from 2016 to 2020 by states
7. *black_state_hc_five_years.csv*: three columns are state, year, and number of anti-Black hate crimes reported each year by states 
8. *asian_state_hc.csv*: two columns are state and sum of number of anti-Asian hate crimes from 2016 to 2020 by states
9. *asian_state_hc_five_years.csv*: three columns are state, year, and number of anti-Asian hate crimes reported each year by states 

**Census + Hate crime data**

10. *census_w_hc.csv*: five years of data by state level with 34 columns including demographic, socioeconomic, and racial hate crime variables
11. *census_w_hc_five_agg.csv*: five years aggregated data by state level with 32 columns including demographic, socioeconomic, and racial hate crime variables.
12. ***census_w_hc_FINAL***: five years of aggregated data by state level with 13 columns including demographic, socioeconomic, and racial hate crime variables. This dataset is mainly used to do analysis.

# Code

1. *Analysis.html*: R markdown file including descriptive analysis and predictive analysis on racial hate crimes in the U.S. Also, data 12 listed above was exported as CSV format.
2. *FBI hate crime data cleaning.ipynb*: Jupyter notebook including codes for FBI data cleaning. The code includes procedures to generate time series data and hate crime data (data 1 - 9 listed above.)
3. *Census FBI data cleaning.ipynb*: Jupyter notebook including codes for census data cleaning. The code includes procedures to generate merged data of census and hate crime data (data 10 - 11 listed above.)

