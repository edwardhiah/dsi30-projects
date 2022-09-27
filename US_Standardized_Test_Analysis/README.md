
# Project 1: SAT & ACT Analysis

## Problem Statement

Being part of the College Board, To find out the states that are having low participation rate to provide more support to improve it

## Executive Summary

### Contents:
- 2017, 2018 & 2019 SAT Data Import and Cleaning
- 2017, 2018 & 2019 ACT Data Import and Cleaning
- Outside Research
- Exploratory Data Analysis
   - Investigate Trends in Data
    1. Which states have the highest and lowest participation rates for the 2017, 2018, or 2019 SAT and ACT?
    2. Which states have the highest and lowest mean total/composite scores for the 2017, 2018, or 2019 SAT and ACT?
    3. Do any states with 100% participation on a given test have a rate change year-to-year?
    4. Do any states show have >50% participation on both tests each year?
    5. What is the largest & smallest changes in participation rate for the tests between year to year?
    6. Shortlist of the states to focus on putting more resouces and efforts

- Data Visualization
   1. Heatmap - Correlation between the SAT & ACT data of 2017, 2018 & 2019
   2. Histogram - SAT & ACT Participation Rate
   3. Boxplot - Range of the Participation Rate, SAT Total Scores & ACT Composite Scores (2017, 2018 & 2019)
   4. Scatter Plot - Score relations between the relative year
   5. Scatter Plot - Correlations relations between scores and participation rate
- Conclusions and Recommendations

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|act_composite_2017|float|combined_final|ACT 2017 mean composite score| 
|act_composite_2018|float|combined_final|ACT 2018 mean composite score| 
|act_composite_2019|float|combined_final|ACT 2019 mean composite score| 
|act_participation_2017|float|combined_final|ACT 2017 participation rate in decimal| 
|act_participation_2018|float|combined_final|ACT 2018 participation rate in decimal| 
|act_participation_2019|float|combined_final|ACT 2019 participation rate in decimal| 
|sat_ebrw_2017|int|combined_final|SAT 2017 average Reading and Writing test score| 
|sat_ebrw_2018|int|combined_final|SAT 2018 average Reading and Writing test score|
|sat_ebrw_2019|int|combined_final|SAT 2019 average Reading and Writing test score|
|sat_math_2017|int|combined_final|SAT 2017 average Math test score|
|sat_math_2018|int|combined_final|SAT 2018 average Math test score| 
|sat_math_2019|int|combined_final|SAT 2019 average Math test score| 
|sat_participation_2017|float|combined_final|SAT 2017 participation rate in decimal| 
|sat_participation_2018|float|combined_final|SAT 2018 participation rate in decimal| 
|sat_participation_2019|float|combined_final|SAT 2019 participation rate in decimal| 
|sat_total_2017|int|combined_final|SAT 2017 mean total score|
|sat_total_2018|int|combined_final|SAT 2018 mean total score|
|sat_total_2019|int|combined_final|SAT 2019 mean total score|
|sat_diff_17_18|float|combined_final|SAT 2017_18 mean total score differences|
|sat_diff_18_19|float|combined_final|SAT 2018_19 mean total score differences|
|act_diff_17_18|float|combined_final|ACT 2017_18 mean composite score differences|
|act_diff_18_19|float|combined_final|ACT 2018_19 mean composite score differences|


### Additional Sources:
1. SAT ACT Score Convertom Tables. ([source](https://www.crimsoneducation.org/sg/blog/test-prep/sat-vs-act-whats-the-difference/))
2. Which States Require the SAT? Complete List. ([source](https://blog.prepscholar.com/which-states-require-the-sat))
3. Which States Require the ACT? Full List and Advice. ([source](https://blog.prepscholar.com/which-states-require-the-act-full-list-and-advice))

## Conclusions and Recommendations

### Conclusion:
1. SAT and ACT test scores are inversely related to their test participation rates, the higher the participation rates the higher the number of score registered is lower.
2. SAT and ACT participation rates are inversely related to each other, which shows that most students tend to take only one or the other test.
3. The SAT scoring between the year are positively correlation, which means that there would not have major fluctuation of the scoring in the different years.
4. From consulting outside sources as to the reasons for the two biggest increases in SAT participation rates, a common factor of cost savings was found between the 3 states which most recently decided to switch from ACT to SAT.
5. Participation in such tests is heavily influenced by state policy towards testing.


### Recommendation
6. Based on the 2019 SAT Scores by Intended College Major, the student SAT scoring above 1203 would like to apply for 97.36% of the major.
7. We shortlist the state that student has the mean total score of above 1200.
8. We further bring down the states shortlisted to four:
   - Minnesota
   - Tenneessee
   - Kansas
   - Missouri
   basing on these four state have good ACT participation rate (inversely related to lower SAT participation rate) and the current state policy open to both SAT and ACT test.  




