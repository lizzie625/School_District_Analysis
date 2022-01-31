# School District Analysis
## Overview  
With Maria's help, we conducted a School District Analysis for the school board. The school board has made us aware that some grades in the students_complete.csv file we have been working with are inaccurate. The Thomas High School ninth grader scores for math and reading had been altered. We needed to go into the data and replace these score with NaN so that the school board can still use the data for accurate state-testing infomration. We replaced the data according to the school boards wishes and then repeated the analysis with the new data.  
## Results  
### Replacing the reading and math scores  
In order for the school board to be able to use this data we had to adjust the data to no longer include math and reading scores from 9th graders at Thomas High School. We used the loc method on the student_data_df (our student data stored in a Pandas dataframe) to select all the reading and math scores from the 9th grade at Thomas High School and replace them with NaN.  
### Repeating the School District Analysis  
We had to first combine our student and school dataframes that we created. Once we did this, we need to calculate the total school count, student count, budget, and average scores, which was given to us in the starter code. We then have to calculate a new student count that no longer includes Thomas High School 9th graders.  
![student_count_recalculated](https://user-images.githubusercontent.com/96501958/151723809-b106b4a6-de41-4773-b163-44053a84ad5f.png)  
We then calculated the passing percentages of our new dataset, the results were as followed:  
* Passing Math Percentage: 74.76%
* Passing Reading Percentage: 85.66%
* Passing both Math and Reading: 25105 students
* Overall Passing Percentage: 64.86%  
### School Summary  
We got the number of 10th-12th graders at Thomas High School using the loc method and created a value that combines the numbers of 10th, 11th, and 12th graders. We then calculated all the students at Thomas High School who passed math, reading, and both math and reading. We also calculated the percentage of students from grades 10th-12th at Thomas High School who passed math, and those who passed reading, as well as, the overall passing percentage.  
![upperclassman_percentages](https://user-images.githubusercontent.com/96501958/151723928-19e8fa86-a5f7-41df-9bec-70cf15b0892b.png)  
Due to the 9th graders at Thomas High School having corrupt grades, which we then replaced with NaN, we need to replace the reading, math, and overall percentages in the school summary with the new values we got omitting 9th graders.  We then filled out the rest of our data sheet with the original code used to determine high and low performing schools, math and reading scores by grade, scores by school spending, scores by school size, and scores by school type. 
## Summary  
4 changes to the school district analysis after reading and math scores have been replaced
