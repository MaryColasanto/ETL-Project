# NBA Extract, Transform, Load

## Project Directive
Extract NBA data from data.world and create several relational SQL tables after normalizing extracted data.

## Dataset
We retrieved NBA player and salary data from data.world at the following web address: https://data.world/datadavis/nba-salaries.

## Extract
We imported the csv files into a Jupyter Notebook and used python/pandas to perform our data transformation. 

## Transform
Types of data transformation included below:  \n
-We edited data of inconsistent formats. For example, we used str.split method in pandas to remove the hyphen from the height column as well as the "lbs" suffix from the weight column. We also used str.split to separate columns with multiple words into separate columns to flatten the structure of our database.  \n
-We used the pandas "func" method to perform mathematical equations on the data - converting the height column from Feet-Inches to aggregated inches.  \n 
-Deleted extraneous columns from the data source we did not feel necessary to include in our final SQL database.  \n

## Load
We loaded our cleaned tables into a SQL database by establishing a connection to a SQL database in Python. From our cleaned data we created 5 SQL tables (column names):
-Demographics (player_id, name, height, birth_year, birth_city, birth_state)
-Salary (player_id, salary, season, team)
-Position (player_id, position, shoots)
-Draft (player_id, draft_pick, draft_round, draft_team, draft_year)
-Schools (player_id, high_school, hs_city, hs_state, college, college_2)

