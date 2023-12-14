# IPL 2008-2022 Analysis Dashboard

### Dashboard Link : https://www.novypro.com/project/ipl-2008-2022-analysis-1

## Problem Statement

This dashboard helps us to understand & analyze IPL cricket statistics from year 2008-2022. Based on the dataset given, we're supposed to present insightful reports where one can access and learn about the key features of all IPL seasons.

Parametes like Venue, Seasons, Batting, Bowling, Boundaries, Season winner and Individual performance are to be taken into consideration.


### Steps followed 

- Step 1 : Acquiring IPL dataset, dataset is a csv file.
- Step 2 : Loading Dataset through SQL server to PowerBI.
- Step 3 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 4 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 5 : It was observed that columns in table IPL_matches_2008_2022 like city, team1, team2, winning_team, there was spelling vagueness. So, used find & replace tools and corrected the names. 
- Step 6 : In the report view, under the view tab, theme was selected. 
- Step 7 : Donut chart were added for four fields named "Matches won based on Toss Decision", "Matches won based on result type"
- Step 8 : several card visuals were added to the canvas, representing, "Season Winner", "Orange Cap", "Purple Cap", "Touranment 6's", "Tournament 4's", "Select Batsman", "Select Bowlers", and "Matches analysis by venue".
- Step 9 : Three Visual Charts(slicers) were added for Season selection, Batsman Selection and Bowler Selection respectively. 

        
- Step 10 : New measure was created to find "Matches won based on Toss Decision".

Following DAX expression was written for the same,
        
        Matches won based on Toss Decision = CALCULATE(COUNTROWS(ipl_matches_2008_2022), ipl_matches_2008_2022[toss_winner] = ipl_matches_2008_2022[winning_team])
             
 - Step 11 : New measure was created to find  "Title Winner",
 
 Following DAX expression was written to find % of customers,
 
         Title Winner = var max_date = CALCULATE(MAX(Calender[Date]), ALLSELECTED(ipl_matches_2008_2022), VALUES(ipl_matches_2008_2022))
var winner = CALCULATE(SELECTEDVALUE(ipl_matches_2008_2022[winning_team]), Calender[Date] = max_date)
return winner
 
 
 - Step 12 : New measure was created to calculate "Bowling_sr".
 
 Following DAX expression was written to find total distance,
 
         Bowling_sr = COUNT(ipl_ball_by_ball_2008_2022[bowler])/SUM(ipl_ball_by_ball_2008_2022[iswicket_delivery])
   

 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard snap](https://github.com/divya-nayan/Dashboards-Reports-Assessments/assets/53559386/1190fdc7-3000-4113-8106-31446c078662)

# Insights

A single page report was created on Power BI Desktop & it was then published to novyPro.com.

Following inferences can be drawn from the dashboard;

### [1] Most Title Winner = Mumbai Indians

   Most number of matches won by = Mumbai Indians

   Most matches Played at Venue = Eden Gardens
   Current IPL title winner of season 2022 = Gujarat Titans
           
           
### [2] Other Insights

   1. Most runs scored by batsman = Virat Kohli (6634 runs)
   2. Most wickets taking bowler =  DJ Bravo.
   3. Total 6's hit = 10.66k
   4. Total 4's hit = 25.49k
   5. Approx 54% matches are won by wickets(chasing), 42% matches are won by runs(batting first), 1% ended with superovers and remaining ended undecided.
  

 
