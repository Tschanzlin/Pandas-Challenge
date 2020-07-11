# Pandas-Challenge

General notes:
- I would have rather done this exercise in Python
- I found the grouping and data manipulation in Panda to be far too complex and cumbersome, but I know that my approach may have been on of the least efficient ways to manipulate the data

Clean-up Items:
- Add 'School type' to schoolsum data
- Format data using the map function
- Format and organize column headers


Late 7/11:
- Use MathPass, ReadPass, and TotPass datafiles to count passsing students, grouped by school to create total count values for each one of those datasets 
- Divide by same column from "group_df" (total counts grouped by school) to calculate passing percentages for each school
- Form dataframes and concatenate

7/11:
- For school summary data:
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
- Unable to calculate % passing with a single command (MathPass = students_df[students_df["reading_score"]>=70].count without returning contents of entire datafram




