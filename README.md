The objective of this project is to scrape, process, analyze, and visualize cricket match data available at Cricsheet. Learners will use Selenium to scrape JSON files of different cricket match types (ODI, T20, Test), store the data in SQL tables, and create a Power BI dashboard to analyze key performance metrics. The project also includes writing 20 SQL queries to uncover insights such as top-performing players, team statistics, and match outcomes.And an EDA using python libraries such as matplotlib,seaborn,plotly.
________________________________________

Business Use Cases
1.	Player Performance Analysis: Analyze players' performance across different match formats (Test, ODI, T20).
2.	Team Insights: Compare team performance over time and across match types.
3.	Match Outcomes: Understand win/loss patterns, margin of victories, and trends.
4.	Strategic Decision-Making: Assist analysts, coaches, and management in making informed decisions.
5.	Fan Engagement: Present interactive dashboards for fans to explore match data and statistics.
________________________________________
Approach
1.	Data Scraping Using Selenium
1.1.	Automate navigation to https://cricsheet.org/matches/.  
1.2.	Use Selenium to scrape and download all the JSON files available on the page.  

2.	Data Transformation
2.1.	Parse JSON files using Python’s pandas library.  
2.2.	Create separate DataFrames for Test, ODI, and T20 match types.  

3.	Database Management
3.1.	Create an SQL database (e.g., MySQL or SQLite).
3.2.	Design separate tables for each match type: test_matches, odi_matches, t20_matches.
3.3.	Test Match Tables
3.3.1.1.	testmatchinfo
Table fields and datatype:
Field	Type
match_id	int
file_id	int
balls_per_over	int
dates_0	date
event_name	varchar(255)
gender	varchar(10)
match_type	varchar(55)
season	varchar(10)
team_type	varchar(55)
teams_0	varchar(55)
teams_1	varchar(55)
toss_winner	varchar(55)
toss_decision	varchar(55)
winner	varchar(55)
by_runs	decimal(5,0)
by_innings	decimal(3,0)
by_wickets	decimal(3,0)
outcome	varchar(55)
outcome_by	varchar(55)
	
3.3.1.2.	Testinningdata:
Contains following fields and datatype:

Field	Type
match_id	bigint
batter	text
bowler	text
non_striker	text
runs_batter	bigint
runs_extras	bigint
runs_total	bigint
file_id	bigint
inning	bigint
Over	bigint
delivery	bigint
team	text
season	text
team_type	text
gender	text
wickets_0_kind	text

3.4.	ODI Match Tables
3.4.1.	odimatchinfo
Contains following fields and datatype:

Field	Type
match_id	int
file_id	int
balls_per_over	int
dates_0	date
event_name	varchar(255)
gender	varchar(10)
match_type	varchar(55)
season	varchar(10)
team_type	varchar(55)
teams_0	varchar(55)
teams_1	varchar(55)
toss_winner	varchar(55)
toss_decision	varchar(55)
winner	varchar(55)
by_wickets	decimal(2,0)
by_runs	decimal(3,0)
outcome	varchar(55)

3.4.2.	odiinningdata
Contains following fields and datatype:

Field	Type
match_id	bigint
batter	text
bowler	text
non_striker	text
runs_batter	bigint
runs_extras	bigint
runs_total	bigint
file_id	bigint
inning	bigint
Over	bigint
delivery	bigint
team	text
season	text
team_type	text
gender	text
extras_wides	double
wickets_0_kind	text

3.4.3.	t20matchinfo
Contains following fields and datatype:

Field	Type
match_id	int
file_id	int
balls_per_over	int
dates_0	date
event_name	varchar(255)
gender	varchar(10)
match_type	varchar(55)
season	varchar(10)
team_type	varchar(55)
teams_0	varchar(55)
teams_1	varchar(55)
toss_winner	varchar(55)
toss_decision	varchar(55)
winner	varchar(55)
by_wickets	decimal(2,0)
by_runs	decimal(3,0)
outcome	varchar(55)

3.4.4.	t20inningdata
Contains following fields and datatype:

Field	Type
match_id	bigint
batter	text
bowler	text
non_striker	text
runs_batter	bigint
runs_extras	bigint
runs_total	bigint
file_id	bigint
inning	bigint
Over	bigint
delivery	bigint
team	text
season	text
team_type	text
gender	text
extras_wides	double
wickets_0_kind	text


4.	SQL Queries for Data Analysis
SQL queries for creating tables and extracting data is written in the below python file.
 SQL_TABLE_&_QUERRY.ipynb

5.	EDA using Python
different visualizations using libraries like matplotlib,seaborn,plotly
All visualizations are created in the query file stated above and visuals. A powerpoint presentation sing the visuals are prepared for the Test Team of Australia. Both visuals and presentation are saved in the file named: Pandas Plots and Presentation
6.	Power BI Dashboard
PowerBI dash board is created for better data visualization and analysis.
04 numbers of Power BI files are created.
I.	For Players
a.	For Test Matches - test_cricsheet_inning .pbix
b.	For ODI Matches - odi_cricsheet_inning.pbix
c.	For T20 Matches - t20_cricsheet_inning.pbix
II.	For Matches
a.	For Match Summary of all formats - match_info_all_format.pbix
All .pbix files are saved in the folder Power BI Files along with the screenshots of some dashboards.
________________________________________
Results
●	Automated scraping of JSON files from Cricsheet.
●	Structured SQL database with separate tables for Test, ODI, and T20 matches.
●	SQL queries to analyze player and team performance metrics.
●	A dynamic Power BI dashboard to present insights visually.
________________________________________
Technical Tags
●	Matplotlib,Seaborn
●	Web Scraping
●	Selenium
●	Python
●	Pandas
●	SQL (MySQL/SQLite)
●	Power BI
●	JSON
●	Data Analysis

