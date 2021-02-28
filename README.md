# PyCity Schools Analysis
---
## Overview of Project

### Purpose

This week’s challenge is to continue using Python in the Junyper Notebook environment to help Maria analyze her school district’s math and reading scores. Python, when used within this environment, can utilize what is known as the Pandas Library which is a list of functions that includes facilitating the creation of tables known as data frames. Data frames can then be used to create other tables, manipulate data as well as visualize the results in an easy to read fashion.

## Results

### Replacing 9th Grade Data at Thomas High School

After a handful of data frames were created to help visualize the test score results for the school district, it was determined that the scores from the ninth graders at Thomas High School may have been falsified in some manner. Therefore, it was necessary to remake the tables to specifically exclude their test results and make comparisons based on the new outcomes.  

1)	Although the ninth graders at Thomas High School make up only about one percent of the total students in the district, excluding their results did have a slight negative impact on the overall district scores: 

District Summary | Including | Excluding
:---|---|---
Average Math Score: | 79.0 | 78.9
Average Reading Score: | 81.9 | 81.9
Passing Math %: | 75.0% | 74.8%
Passing Reading %: | 86.0% | 85.7%
Overall Passing %: | 65.0% | 64.9%  
 
2)	Other district metrics were also affected but not to a significant degree:  

Metric | Including | Excluding
:---|---|---
District 9th Grade Overall Passing %: | 65.34% | 64.23%
Overall Passing % (Spending Range: $630 to $644): | 62.86% | 62.78%
Overall Passing % (School Size: 1000-2000): | 90.62% | 90.56%
Overall Passing % (Type: Charter School): | 90.43% | 90.39%  

3)	However scores at Thomas High School remained relatively unchanged even after excluding the 9th grade scores:  

Thomas High School | Including | Excluding
:---|---|---
Average Math Score: | 83.36 | 83.35
Average Reading Score: | 83.85 | 83.90
Passing Math Percentage: |93.27% | 93.19%
Passing Reading Percentage: | 97.31% | 97.02%
Overall Passing Percentage: | 90.95% | 90.63%

### Conclusion

Ultimately, while overall district scores did decrease slightly across the board when the reading and math scores for ninth graders at Thomas High School were excluded, the fact that they did not appear to significantly impact the overall scores at Thomas High School casts some doubt on the accusation that the ninth-grade scores are outliers and/or illegitimate. Moreover, Thomas High School ranked second (both including and excluding ninth-grade scores) in the district based on score results. As such, district averages will decrease if any of their data, regardless of grade, is excluded from the overall district data. Thus, based on test scores alone, it does not appear to show that the ninth-grade score data at Thomas High School indicates cheating. 

### Summary

In this exercise, it was important to accurately update the data to reflect the new student numbers without ninth graders from Thomas High School. If not done correctly, the results would not provide for an apples-to-apples comparison and thus any conclusions would likely be flawed. For example, after the reading and math scores were replaced with null values, without also updating for the reduced number of students at Thomas High School, their results would have reflected inaccurate pass percentages as seen here:

[![THS-Before-Replacement.png](https://i.postimg.cc/gcLS7PRW/THS-Before-Replacement.png)](https://postimg.cc/23m7qM2c)  


Updated data frame to account for correct student values:  

[![THS-After-Replacement.png](https://i.postimg.cc/WzcMKxLN/THS-After-Replacement.png)](https://postimg.cc/Hc3c8ZkR)  


Without replacing the “% Passing Math”,”% Passing Reading” and “% Overall Passing” to reflect their true values, Thomas High School would have been ranked as a medium performing school (instead of the second highest performing), and their overall scores would have also negatively skewed results for medium-sized schools (65% vs 91%) as well as scores for charter schools (65% vs 90%) thus clouding the conclusions that can be made when the data is not corrupted (see charts below).

[![School-Size-Results.png](https://i.postimg.cc/ZKcr7ffm/School-Size-Results.png)](https://postimg.cc/PPCpNMsV)  


[![School-Type-Results.png](https://i.postimg.cc/x89XLQVz/School-Type-Results.png)](https://postimg.cc/PpFfkBxX)  
