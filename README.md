#                                   Module 4 :  Pandas Assignment

## Introduction: 

 As the new Chief Data Scientist for city's school district. In this capacity, you'll be helping the school board and mayor make strategic decisions regarding future school budgets and priorities. As a first task, analyze the district-wide standardized test results. You have been given access to every student's math and reading scores, as well as various information on the schools they attend. Your task is to aggregate the data to showcase obvious trends in school performance.

 ## Instructions:

Using Pandas and Jupyter Notebook, create a report that includes the following data. Your report must include a written description of at least two observable trends based on the data.

# District Summary
Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.
Total number of unique schools
Total students
Total budget
Average math score
Average reading score
% passing math (the percentage of students who passed math)
% passing reading (the percentage of students who passed reading)
% overall passing (the percentage of students who passed math AND reading)

# School Summary
Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.
School name
School type
Total students
Total school budget
Per student budget
Average math score
Average reading score
% passing math (the percentage of students who passed math)
% passing reading (the percentage of students who passed reading)
% overall passing (the percentage of students who passed math AND reading)

# Highest-Performing Schools (by % Overall Passing)
Sort the schools by % Overall Passing in descending order and display the top 5 rows.
Lowest-Performing Schools (by % Overall Passing)
Sort the schools by % Overall Passing in ascending order and display the top 5 rows.
Save the results in a DataFrame called "bottom_schools".
Math Scores by Grade


# Average Math Score for students of each grade level (9th, 10th, 11th, 12th) at each school.

# Reading Scores for students of each grade level (9th, 10th, 11th, 12th) at each school.

# Scores by School Spending
Create a table that breaks down school performance based on average spending ranges (per student).

# Use the code provided below to create four bins with reasonable cutoff values to group school spending.
                    spending_bins = [0, 585, 630, 645, 680]
                    labels = ["<$585", "$585-630", "$630-645", "$645-680"]
                    Use pd.cut to categorize spending based on the bins.

# Use the following code to then calculate mean scores per spending range.
                    spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
                    spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
                    spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
                    spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
                    overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()
                    Use the scores above to create a DataFrame called spending_summary.


# Scores by School Size
Use the following code to bin the per_school_summary.
                    size_bins = [0, 1000, 2000, 5000]
                    labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
                    Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.


# Scores by School Type
Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.
            This new DataFrame should show school performance based on the "School Type".
