# School District Analysis
## Overview  
With Maria's help, we conducted a School District Analysis for the school board. The school board has made us aware that some grades in the students_complete.csv file we have been working with are inaccurate. The Thomas High School ninth grader scores for math and reading had been altered. We needed to go into the data and replace these score with NaN so that the school board can still use the data for accurate state-testing infomration. We replaced the data according to the school boards wishes and then repeated the analysis with the new data.  
## Analysis 
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
## Results  
* The data involved 39170 students, after we took out the Thomas High School 9th graders, we are left with 38709 students. The district summary was not largely affected after the changes we made to the dataset.  The images below show no more than a .3 different in scoring between the old data and the reconstructed data.   
![original_district_summary](https://user-images.githubusercontent.com/96501958/151726733-c57f5469-766a-4997-98a5-9b7853bf81a5.png)  Figure 1. original district summary results  
  
![new_district_summary](https://user-images.githubusercontent.com/96501958/151726734-0102760f-0229-4909-ba8b-42082cdf47b4.png)  Figure 2. updated district summary results  
* The school summary was also affected little, but these changes are easier to see as you go through the dataset. Thomas High School originally had an overall passing percentage of 90.95, when the data is first adjusted it becomes 64.85 when including the NaN scores. Thomas High School's performance is affected again by taking the 9th graders out of the dataset, resulting in an overall passing percentage of 90.63. Below shows the school summary before, during, and after adjusting the dataset to exclude the freshman, respectfully.  
![old_school_summary](https://user-images.githubusercontent.com/96501958/151728422-cbd4dcab-b09d-4d75-83de-b50f7582e254.png)  
![new_school_summary](https://user-images.githubusercontent.com/96501958/151728424-5d9a0db7-6b5f-411e-800c-b9538aee144d.png)  
![new_school_summary_upperclassmen](https://user-images.githubusercontent.com/96501958/151728884-0ea9e6a9-5a65-4a26-adc5-ce7cc53db1af.png)  

* Removing 9th graders from the data affects math and reading scores by grade little. The new data shows passing math % is 74.76, passing reading score is 85.66%, and passing both math and reading is 25105 students. The original ninth grade math scores for THS were 83.59, reading were 83.73. The original passing math % is 74.98, passing reading % is 85.81, both math and reading students is 25528. There is roughly a .2% difference in passing percentages when the 9th graders are removed from the data versus when the original grades are in the data.  
  
* Math and reading scores by grade are not largely affected for anything other than Thomas High School 9th graders. However, for the THS 9th graders it is significantly affected. This is do to all of the grades being replaced with NaN in the dataset, making the scores go from roughly 83 to null for both reading and math.  
![math_reading_by_grade](https://user-images.githubusercontent.com/96501958/151732347-e09bd023-93ea-4ef8-a782-2321839776db.png)  
  
* The school spending was not significantly affected either. The images below show the results for school spending for the original data as well as the new data 
![old_school_spending](https://user-images.githubusercontent.com/96501958/151726760-ece701b5-0bcf-4dcf-938f-0c6c50f6b4ca.png)  
![new_school_spending](https://user-images.githubusercontent.com/96501958/151726808-049f3c3c-3190-4a20-8775-1299ee3a1ca7.png)  
  
* The removal of 9th graders from Thomas High School in the dataset has no significant effect on scores by school size or scores by school type, shown below. 
![old_School_size](https://user-images.githubusercontent.com/96501958/151726650-650d62dd-cd0f-4f27-be77-7623e6bc9f81.png)  
Figure 3. original school size data  
![new_school_size](https://user-images.githubusercontent.com/96501958/151726680-8ba165ab-ff58-41ff-aab3-24293338881f.png)  Figure 4. school size data with the removal of THS 9th graders  

![old_school_type](https://user-images.githubusercontent.com/96501958/151726706-e50554a2-7ebe-4159-ab88-1b699bd67033.png)  Figure 5. original dataset showing school type analysis  
![new_school_type](https://user-images.githubusercontent.com/96501958/151726716-ec270c91-fcf4-4952-9755-d6e444a24480.png)  Figure 6. school type results of the new dataset  

## Summary  
After adjusting the dataset for the school board, we can see there is not a significant change in the data on a large scale. However, there are reductions in the percent passing math, percent passing reading, and overall passing percentage. This could hint towards the academic dishonesty that the school board was worried about. We also see a increase in per student budget in the dataset after we removed the 9th graders, now the school looks as though it has less students, but the same amount of money was spent. The 9th grade student data is also significantly affected because the scores for Thomas High School are NaN. The 9th grade data across schools is therfore affected. 
