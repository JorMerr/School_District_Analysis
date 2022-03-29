# School_District_Analysis

## Overview of the Project

The purpose of this project was to refactor code to ensure the school board and Maria would be able to continue analysis of board wide math and reading test scores after evidence of academic dishonesty was discovered related specifically to Thomas High School ninth grade scores.

Maria would like the data from the Thomas High School ninth graders replaced with NaN while she and her supervisor continue to analyze the reamining data with the ninth grader's information replaced. The school board will continue investigations to determine the extent and scope of the academic dishonesty.

## Results

### District Summary After Changes

- The district summary of math and reading scores has been affected by replacing all Thomas High School scores in math and reading with NaN in the following ways:

	- The "Average Math Score" for the district *fell* from **79.0% to 78.9%**.

	- The "Average Reading Score" *remained unchanged* at **81.9%**.

	- The "% Passing Math" figure *fell* from **75.0% to 74.8%**.

	- The "% Passing Reading" figure *fell* from **86.0% to 85.7%**.

	- The "% Overall Passing" figure *fell* from **65.0% to 64.9%**.

See below the initial District Summary table:
![Original District Summary](https://github.com/JorMerr/School_District_Analysis/blob/main/Resources/district_summary_df_original.PNG)

See below the updated District Summary table after replacing Thomas High School ninth grade scores:
![New District Summary](https://github.com/JorMerr/School_District_Analysis/blob/main/Resources/new_district_summary_df.PNG)

### School Summary After Changes

- The summary of math and reading scores per individual school has been affected by replacing Thomas High School ninth grade scores with NaN in the following ways:

	- Brief comparison of the per_school_summary_df tables before and after the replacement of Thomas High School ninth grade scores shows the only figures which have been altered are those belonging to Thomas High School. This is as intended, given the request by the school board to replace only the ninth grade scores for Thomas High School.

See the Original Per School Summary below:
![Original Per School Summary](https://github.com/JorMerr/School_District_Analysis/blob/main/Resources/original_per_school_summary_df.PNG | width=100)

See the Updated Per School Summary below:
![Per School Summary with 9th Grade NaN Values Not Included](https://github.com/JorMerr/School_District_Analysis/blob/main/Resources/new_per_school_summary_df_2.PNG | width=100)

### Changes Specific to Thomas High School

- Replacing Thomas High School ninth grade scores resulted in the following changes to Thomas High School's scores and standing (As seen in the above images):

	- "Average Math Score" *fell* from **83.41% to 83.35%**.

	- "Average Reading Score" *increased* slightly from **83.84% to 83.89%**.

	- "% Passing Math" *fell* from **93.27% to 93.18%**.

	- "% Passing Reading" *fell* from **97.30% to 97.01%**.

	- "% Overall Passing" *fell* from **90.94% to 90.63%**.


	- Thomas High School remains in the Top 5 schools with the second highest overall passing rate of schools when the scores for only 10th, 11th, and 12th graders are considered. It is expected that should the 9th graders' scores be included with the replaced NaN values being considered as 0, Thomas High School would not remain in the current standings. For the purposes of this report, the calculations excluded all ninth grade scores for Thomas High School until further clarity can be obtained regarding the alleged academic dishonesty.
	- As can be seen in the following image, the inclusion of the replaced ninth grade scores results in significant changes to the percentage of passing students at Thomas High School. This information is potentially a misrepresentation of the data as the academic dishonesty may be limited to a very few number of students.

![Thomas High School Summary with NaN Values Included](https://github.com/JorMerr/School_District_Analysis/blob/main/Resources/ths_ninth_incl_per_school_summary.PNG)


### Further Analysis After Changes
- The replacement of Thomas High School's ninth grade scores results in the following changes elsewhere in the analysis:

	- Math and reading scores by grade remain unchanged for all but the Thomas High School ninth grade scores, replaced by "NaN". Click to view original scores for [math](https://github.com/JorMerr/School_District_Analysis/blob/main/Resources/original_math_scores_by_grade.PNG) and [reading](https://github.com/JorMerr/School_District_Analysis/blob/main/Resources/original_reading_scores_by_grade.PNG). Click to view updated scores for [math](https://github.com/JorMerr/School_District_Analysis/blob/main/Resources/new_math_scores_by_grade.PNG) and [reading](https://github.com/JorMerr/School_District_Analysis/blob/main/Resources/new_reading_scores_by_grade.PNG).

     - The changes to Thomas High School's ninth grade scores did not impact the school board's overall results based on school spending.

     - The changes to Thomas High School's ninth grade scores did not impact the school board's overall results based on school size.

     - The changes to Thomas High School's ninth grade scores did not impact the school board's overall results based on school type.



## Summary

After the changes were made to Thomas High School's 9th grade math and reading scores, the analysis shows several changes.

First, the scores and percentage of passing students fell overall with the exception being the "Average Reading Score" has remained unchanged.

Second, the scores and percentage of passing students for Thomas High School in particular fell overall, with the exception of the "Average Reading Score" increasing slightly. Initial assumptions regarding the academic dishonesty may be drawn that changes to scores may be limited primarily to 9th grade math scores, given the overal increase to Thomas High School Average Reading Scores. Further analysis and confirmation from the school board's investigation may be required to corroborate.

Third, the largest change to our analysis after changing Thomas High School's 9th grade scores to NaN for both math and reading is that we are no longer using any of the 9th grade data for Thomas High School. While this is a small subset of our overall data, and has made small impacts overall, this means we may be excluding scores from students who were not involved in academic dishonesty in any way.

Finally, for the purposes of illustrating the reason we exclude our Thomas High School scores in math and reading for 9th grade students, we can see that when those values are included in our overall analysis, a significant portion of Thomas High School's students effectively received a 0 score on their assessment. When the 9th grade scores are included in our calculations, this greatly impacts Thomas High School's results, giving us a "% Overall Passing" erroneous result of 65.07%.

See the image below for the summary of Thomas High School's results when the 9th grade NaN values are included:
![9th Grade NaN Values Included](https://github.com/JorMerr/School_District_Analysis/blob/main/Resources/ths_ninth_incl_per_school_summary.PNG)

## Additional Information

#### Challenges
- Jupyter notebook encountered consistent and repeated "kernel busy" issue when testing .loc[] method
	- resolved as reference error when writing code was corrected.


