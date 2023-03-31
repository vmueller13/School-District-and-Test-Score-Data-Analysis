# pandas-challenge
PyCity Schools

For this challenge, I started out on my own for the first part of the District Summary, then I found the starter code and used that to help structure the rest of my code.

District Summary*


First, I started by using nunique to count the total number of schools in the in the data frame column 'school_name. I used the len function to find the number of students and the sum function for the total budget. Next, I used .mean to calculate the mean of the reading and math scores. The code for the pass percentage for math, reading and overall was given by the starter code, but when I wrote it on my own, I did not divide by float(student_count). After reviewing the starter code, I was able to see my mistake. Lastly, I created a DataFrame for the district summary by passing in all the counts I just created with different column names.

School Summary*


To calculate the counts for school summary, the first step was to set the school type first, then calculating the student count, budget, aveage math & reading scores per school by creating new frames for each subset of data. Next, I looked at all the schools with math scores and reading scores of 70 or higher(in separate outputs) by using >=70. Lastly, I passed all of these counts into a new DataFrame for the per school summary and displayed it.

Highest-Performing School (by% Overall Passing) & Lowest-Performing School (by% Overall Passing)


To calculate the highest performing schools, I started by sorting the schools by % overall passing in descending order (ascending = False) so that I could see the highest performing schools in the data set. Similarly, to caluclate the lowest performing schools, the data is sorted in ascending order (ascending = True) to show the lowest performing schools in the data set.

Math Scores by Grade and Reading Scores by Grade


The code for these sections is very similar. First, I used the starter code provided to separate the data by grade. From here, I used the groupby function to group by school name and then .mean to find the average for each of the high school grades (9th-12th). Each of these scores were then combined into a single DataFrame, math_scores_by_grade or reading_scores_by_grade that would show the summary table with the average score for each grade.

Scores by School Spending**


For this section, I started with the bins and labels provided by the starter code, made a copy of the per_school_sumary and renamed it as school_spending_df. This allowed me to utilize the "Per Student Budget" column. Next, I had to replace the $ in that column, because otherwise I got an error. Once I changed the type to a float and then to an integer, the code ran without any problems. I used pd.cut to categorize the spending based on the bins, which gave the spending ranges per student. I calculated the math, reading, overall and % passing averages for the 'Spending Ranges Per Student' column and assembled the data into a data frame.

Scores by School Size & School Type


For these sections, I followed very similar steps to the previous section, however, I did not have to replace any special characters and there were no major bugs in my code. First, I utilized the bins and labels from the starter code and categorized the spending based on the 'Total Students' column of the DataFrame. I used pd.cut to accomplish this, and once the per_school_summary was created, I could calculate the average for the School Size and School Type and create new DataFrames.

*For these sections, I worked with fellow bootcamp member, Kimberly Reitama.
**For these sections, I worked with fellow bootcamp member, Saroja Suresh.

Conclusion


From the sections on the lowest performing schools and highest performing schools, I was able to make several interesting conclusions and comparisions. First, these showed that 80% of the top ten performing schools were all charters and 70% of the lowest performing schools were all districts. This might have been the data that was expected by school type, but upon further analysis, the school type is not necessarily what determined the passing rates. 
While the per student spending is very similar for the charters and the districts, 87% of charters were categorized as small or medium schools while 100% of the districts were categorized as large schools. Additionally, even though both school types spent similar amounts per student, the small and medium sized schools (both charter and district) consistently showed a higher achievement and overall passing rate.

Secondly, it is interesting to note that even though the top eight highest performing schools were charters, they only out performed the district on their average math score by about 7% and reading by about 3%. The overall pass rate, however, shows the districts at 53% and the charters at 90%. This disparity in average achievement further shows the difference between the school sizes and the affect on student achievement.

Since the small and medium sized school consistently out performed the larger schools in every metric for both math and reading, one might conclude that smaller school sizes contribute greatly to the success of their students.



