# Pandas-Challenge

Conclusions -- Data indicates:
- Charter schools significantly outperform district schools
- Small schools (likely charters) outperform larger schools
- The lower spending per student, the better the outcome.  This is probalby due to charter schools receiving less state funding per student, yet outperforming district schhools

Overall Comments:

This was a more challenging exercise than I orginally anticipated.  The first table, the summary of total District statistics, was fairly easy to calculate and format.  However, the second table, the summary of District statistics by school presented two challenges -- filtering tha data for passing grades to calculate the % passing scores by school and re-assembling all of the data into a single table. I found most of the other data was easly to prepare using the groupby function and the applying count() or mean() to determine the required values for teh relevant series. 

I considered three ways to compile the % passing scores:
- Using list comprehension to read through the columns and calculate averages subject to and if statement 
- Creating loops in python to run the calculations
- Using ".loc" to filter the dataframes by passing grades > 70

The first two seemed more complicated than what was required by the assignment, although I would like to explore this further.  The last alternative would not work.  I wasn't able to use the ".loc" function to screen a series by a number, even though the datatype was int64.  The error either referenced a string/int mismatch or an invalid operator type with ">=".  Ulitimately, I realized I had been able to create dataframes for the first table that filtered test scores below 70, and used those dataframes to calculate passing math, reading, and overall scores.

I also struggled to re-assemble the data as I built out some of the correct series.  I considered using the merge function, but thought the concatenate function would be better suited.  At first, the output was out of order and I had difficultly formatting the headers correctly.  The whole exercise was simplified when it occurred to me that I was just creating series of dictionaries with the keys indexed to the school name. 

All required values for each of the tables have been presented and are calculated correctly.  However, I still need to work on some of the formatting.

Remaining clean-up items:
- School Summary:  Alhpa sort on index 
- Math / Reading Scores:  Work on reformatting to match requested output
- Other:  See if code can be further simplified; clean up calculations of intput for schoolsum_df 

7/12:
- Lightbulb moment - calculated values stored as a dictionary.  Set index to "school_name" to create dictionary with school names as keys and individual series values  referenced to the school 
- Summary chart complete and calculated correctly

Late 7/11:
- Use MathPass, ReadPass, and TotPass datafiles to count passsing students, grouped by school to create total count values for each one of those datasets 
- Divide by same column from "group_df" (total counts grouped by school) to calculate passing percentages for each school
- Form dataframes and concatenate

7/11:
-For school summary data:
> Create master group by file, grouped by school name
> Create df using mean function to determine avg size, budget, reading / math score
> Create df using loc function to calculate % passing when grades > 70
> Combine datafiles using the concatenation function

- Created sub-sets of the original dataframe filtered by math and reading scores >=70 and then ran count and average scores off that
- For total passing stats, I assumed students had to path mass and reading, and so ran the analysis by filter ReadPass further by passing math scores
 

7/10:
- Building basic outline of the analysis
- Imported schools and students datafiles; evaulated format
- Merged files in order to calculate student scores by district (may not need to do this as disctrict appears to mean by school and not by district type)
- Calculated basic stats (Totals and Averages) for the total district
- Unable to calculate % passing with a single command (MathPass = students_df[students_df["reading_score"]>=70].count without returning contents of entire dataframe




