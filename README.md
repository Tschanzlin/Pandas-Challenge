# Pandas-Challenge

Conclusions -- Data indicates:
- Charter schools significantly outperform district schools
- Small schools (likely charters) outperform larger schools
- The lower spending per student, the better the outcome.  This is probalby due to charter schools receiving less state funding per student, yet outperforming district schhools

Overall Comments:
This was a more challenging exercise than I orginally anticipated.  The first table, the summary of total District statistics, was fairly easy to calculate and format.  However, the second table, the summary of District statistics by school presented two challenges -- filtering tha data for passing grades to calculate the % passing scores by school and re-assembling all of the data into a single table. I found most of the other data was easy to prepare using the groupby function and applying count() or mean() to determine the required values for the relevant series. 

I considered three ways to compile the % passing scores:
- Using list comprehension to read through the columns and calculate averages subject to and if statement 
- Creating loops in python to run the calculations
- Using ".loc" to filter the dataframes by passing grades > 70

The first two seemed more complicated than what was required by the assignment, although I would like to explore this further.  The last alternative would not work.  I wasn't able to use the ".loc" function to screen a series by a number, even though the datatype was int64.  The error either referenced a string/int mismatch or an invalid operator type with ">=".  Ulitimately, I realized I had already created dataframes for the first table that filtered test scores below 70, and used those dataframes to calculate passing math, reading, and overall scores.

I also struggled to re-assemble the data as I built out some of the correct series.  I considered using the merge function, but thought the concatenate function would be better suited.  At first, the output was out of order and I had difficultly formatting the headers correctly.  The whole exercise was simplified when it occurred to me that I was just creating series of dictionaries with the keys indexed to the school name. I either specically indexed the data to the school name, or relied on the group function to index.

All required values for each of the tables calculate correctly.  However, there are some small formatting differences.  I also used a double group function to prepare the math and reading scores by grade by school that present the data differently, but which was the most efficient way I could think of to calculate the data.  I would like to explore ways to futher simplify some of the code.

Notes:
7/12:
- Lightbulb moment - calculated values stored as a dictionary.  Set index to "school_name" to create dictionary with school names as keys and individual series values referenced to the school 
- Summary chart complete and calculated correctly

Late 7/11:
- Use MathPass, ReadPass, and TotPass datafiles to count passsing students; group by school to create total count values for those datasets and divide by total student count for each school
- Form dataframes and concatenate

7/11:
-For school summary data:
> Create master group by file, grouped by school name
> Create df using mean function to determine avg size, budget, reading / math score
> Create df using loc function to calculate % passing when grades > 70 (not working)
- Created sub-sets of the original dataframe filtered by math and reading scores >=70 and then ran count and average scores off that
- For total passing stats, I assumed students had to path mass and reading, and so ran the analysis by filter ReadPass further by passing math scores

7/10:
- Building basic outline of the analysis
- Imported schools and students datafiles; evaulated format
- Merged files in order to calculate student scores by district (may not need be necessaery)
- Calculated basic stats (Totals and Averages) for the total district
- Unable to calculate % passing with a single command (MathPass = students_df[students_df["reading_score"]>=70].count without returning contents of entire dataframe




