# Pandas-Challenge

General notes:
- Given the length of file and number of cells, I chose to use a "#" to de-activate many of the check functions I used at the end of each cell, except where the final output was rendered
- I would have rather done this exercise in Python
- I found that the approach I used in Panda to group and manipulate the data was far too complex and cumbersome for this exercise, but I'm certain there is an easier way to do this.
- I considered three ways to create the school district summary data:
> Using list comprehension to read through the columns and calculate averages
> Creating loops in python to run the calculations
> Using ".loc" to filter the dataframes by passing grades > 70
> Using the grouping functions to group and filter datafiles, and then re-assemble into a final ouptut file
- I wasn't able to use the ".loc" function to filter, getting a string / int error, despite confirming the math_score and reading_score columns were number datatypes
- Ultimately, I used the last version as I wasn't sure how to use the list comprehension function on a large datafile, and in the case of Panda, wasn't sure i could re-assemble the data into dataframes without manually creating a dictionary for each school
- Realize now that the easiest approach is to create a dictionairy for each column where the key is the school name, and the value is the variable for the particular series ("School Type", "Total Students", etc.). Still trying to determine whether each series would need to be indexed to the school_name.  I believe this is the case.  Once dictionaries are created, then it's simply a matter of making a new dataframe assembling all of the dictionairies.


Clean-up Items:
- Add 'School type' to schoolsum data
- Format data using the map function
- Format and organize column headers
- Go back and see if there's a simpler way to assemble the first row of data

7/12:
- Lightbulb moment - calculated values stored as a dictionary.  Set index to "school_name" to create dictionary with school names as keys and individual series values  referenced to the school 

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




