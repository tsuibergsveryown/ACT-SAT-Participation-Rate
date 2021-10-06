### Project 1 Overview ###
The scenario is if I was hired by the state of California to find out which school district(s) need the most help from the states government, so that the state of California can properly allocate the resources to the schools that need the most to increase the ACT/SAT participation rate and ultimately the test scores. 

Increasing the test scores of more students can increase the rate of undergraduate participation, which
increase the amount of tuition borrowed & spent. This could generate future income for the states of 
California. 

### Data Science Problem Statement ###
Where in the state of California does the state government need to allocate the resources to, 
in order to help increasing test participation and test scores? Here, I'm suggesting the top 10
school districts to allocate the resources to based 3 factors: 
1. the lowest percentage test taking rate, 
2. the lowest percentage of students who scored more than 21 points on ACT, 
3. and the lowest percentage of students who met or exceed the benchmark for SAT. 

All data are from 2019, and only on grade 12 students.

### Datasets ###

** Original Datasets **
[`act_2019.csv`](./data/act_2019.csv)
[`sat_2019_ca.csv`](./data/sat_2019_ca.csv)

** Cleaned & Organized Datasets **
(based on the above 2 datasets)
[`act2019ca_complete.csv`](./code/act2019ca_complete.csv) 2019 ACT Scores in California by School, with no empty cells
[`act2019ca_big.csv`](./code/act2019ca_big.csv) 2019 ACT Scores in California by School, with schools that have more than 15 students taking the test
[`act2019ca_small.csv`](./code/act2019ca_small.csv) 2019 ACT Scores in California by School, with schools that less than 15 students taking the test
[`sat2019ca_complete.csv`](./code/sat2019ca_complete.csv) 2019 SAT Scores in California by School, with no empty cells
[`sat2019ca_big.csv`](./code/sat2019ca_big.csv) 2019 SAT Scores in California by School, with schools that have more than 15 students taking the test
[`sat2019ca_small.csv`](./code/sat2019ca_small.csv) 2019 SAT Scores in California by School, with schools that have less than 15 students taking the test


### Data Dictionary ###
|Feature|Type|Dataset|Description|
|---|---|---|---|
|s_code|float|ACT|School Code. We use this as the Primary Key in all dataframes|
|s_name|object|ACT|School name|
|d_name|object|ACT|Disctrict Name|
|c_name|object|ACT|County Name| 
|enroll12|float|ACT|Grade 12 Enrolment, based on the number of students enrolled in grade 12.|
|num_tst_takr|floatt|ACT|Number Tested, is the number of students with ACT exam scores as reported.|
|avg_scr_read|float|ACT|Average Score for Reading part of ACT.|
|avg_scr_eng|float|ACT|Average Score for English part of ACT.|
|avg_scr_math|float/|ACT|Average Score for Math part of ACT.|
|avg_scr_sci|float|ACT|Average Score for Science part of ACT.|
|num_ge21|float|ACT|Number of Scores >=21, is the number of students who scored 21 points or more on the composite score.|
|pct_ge21|float|ACT|Percent of Scores >=21, is the percent of students who scored 21 points or more on the composite score by dividing the Number of Scores >=21 by the Number Tested.|
|pct_tst_takr|float|ACT|Percent of Test Taker, is the percentage of how many grade 12 students took of ACT out of all the grade 12 enrolment. It is the num_tst_takr divided enroll12.|
|s_code|float|SAT|School Code. We use this as the unique Primary Key in all dataframes.|
|s_name|object|SAT|School name.|
|d_name|object|SAT|Disctrict Name.|
|c_name|object|SAT|County Name.|
|enroll12|floatt|SAT|Grade 12 Enrolment, based on the number of students enrolled in grade 12.|
|num_tst_takr12|float|SAT||Number Tested, is the number of students with SAT exam scores as reported.|
|num_erw_bmark12|float|SAT|The number of students who met or exceeded the grade 12 ERW benchmark.|
|pct_erw_bmark12|float|SAT|Percent of students who met or exceeded the grade 12 ERW benchmark.|
|num_math_bmark12|float|SAT|The number of students who met or exceeded the grade 12 Math benchmark.|
|pct_math_bmark12|float|SAT|Percent of students who met or exceeded the grade 12 Math benchmark.|
|tot_num_both_bmark12|float|SAT|Grade 12 Total Number Meeting Both Benchmarks. The number of students who met or exceeded both the ERW and mathematics benchmarks for grade 12.|
|pct_both_bmark12|float|SAT|Grade 12 Percent Meeting Both Benchmarks. The percent of students who met or exceeded both the ERW and mathematics benchmarks for grade 12. |
|pct_tst_takr|float|SAT|Percent of Test Taker, is the percentage of how many grade 12 students took of SAT out of all the grade 12 enrolment. It is the num_tst_takr12 divided enroll12.|


### Conclusion ###
As we can see from the data, the more students to participate in the ACT & SAT tests, the more students met or exceed the benchmark for the tests. The state of California should focus on, and allocate the resources appropriately, to the school districts / schools that need the most help. To increase the participation rate, we should be able to see the trend of more students scoring higher and meeting the expectation score level. There are total of 11 school districts that have more than 50% of participation on ACT, and 328 school districts that have >50% participation on SAT. This shows that it's very possible to get the lower schools to catch up. 


### Recommendation ###
The 20 school districts that need the most help from the state's government in order to increase its students test participation rate in both ACT & SAT are:
- ACT
    - Kern High, Antelop Valley Union High, Oxnard Union High, Hemet Unified, Fresno Unified, Colton Joint Unified, Chino Valley Unified, Chaffee Joint Union High, Central Unified, and Anahem Union High
    - These school districts have 2.2% - 4.1% of test participation rate
- SAT
    - William S. Hart Union High, West Covina Unified, Waterford Unified, San Juan Unified, San Diego Unified, Ripon Unified, Los Angeles Unified, Lompoc Unified, East Side Union High, and Borrego Springs Unified
    - These school districts have 4.6% - 12% of test participation rate
    
There are total of 20 school districts and 24 schools that absolutely need help from the state of California to increase the students’ test participate

In comparison to the Nation Means (ACT = 58.5%, SAT = 49%), these schools and school districts have a long way to go. 
In comparison to California Means (ACT = 23%, SAT = 63%), the state of California clearly do not value ACT as much as SAT. 