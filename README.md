# Pandas-Challenge

General notes:

7/11:
- Created sub-sets of the original dataframe filtered by math and reading scores >=60 and then ran count and average scores off that
- For total passing stats, I assumed students had to path mass and reading, and so ran the analysis by filter ReadPass further by passing math scores
- Originallyl thought I would have to use a groupby / getgroup function or even potentially bin the data, but filtering on % passing information either by using a groupby / getgroup function or potentially binning the data  

7/10:
- Building basic outline of the analysis
- Imported schools and students datafiles; evaulated format
- Merged files in order to calculate student scores by district (may not need to do this as disctrict appears to mean by school and not by district type)
- Calculated basic stats (Totals and Averages) for the total district
- Unable to calculate % passing with a single command (MathPass = students_df[students_df["reading_score"]>=80].count without returning contents of entire datafram


Potential items to improve in python files include:
- Simplifying code to include function references if relevant
- Eliminating initial variable definitions if initial value not required

