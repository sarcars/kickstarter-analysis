# Kickstarting with Excel

## Overview of Project

### Purpose
This analysis was created to understand the results of historic Kickstarter campaigns in the theater category.  Data is available for Kickstarter campaigns from May 2009 through May of 2017 detailing information such as campaign financial goal, amount pledged, dates of campaign, and number of backers.  Analysis of this data allows us to make some conclusions on what has been successful and possible areas to pay attention to for those plays that have not met their goals.
## Analysis and Challenges
Analysis on the Kickstarter campaigns for theater (and specifically plays) was made by looking at the data in two different ways.  The first based on the month the campaign launched, and the second at the success or failure of the campaign based on the dollar amount at which the goal was set. 
### Analysis of Outcomes Based on Launch Date
![Theater Outcomes vs Month of Launch](/resources/Theater_Outcomes_vs_Launch.png)
Using a pivot table, I was able to count the number of campaigns that were launched each month and then show these numbers by the outcome of successful, failed, or canceled.  Pivot tables are very useful when counting large amounts of data and using filters can show all this data in a more digestible format.  
### Analysis of Outcomes Based on Goals
![Outcomes Based on Goal Grouping](/resources/Outcomes_vs_Goals.png)
This data is showing the number and percentage of campaigns successful or failed based on the amount that was set for the goal.  To analyze the data I used the `COUNTIFS()` function to sort only campaigns for plays by outcome and goal amount.  
### Challenges and Difficulties Encountered
-Creating pivot tables and graphs was not particularly difficult although experimenting with data in columns or rows as well as the display of the chart can show different results.  Sometimes you need to switch the order of the fields in the row or change the field setting to something other than `Sum` such as `Count` or `Average`  
-I have used the `COUNTIFS()` function before, but this was the first time using more than one criteria and I found it a challenge to get the syntax correct, but once I got one correct, it was really nice that Excel allows you to easily replicate the formula and change what needs to be done. I was not sure if the last row `greater than 50000` was supposed to be `greater or equal to` or not so I did a check of my work by showing the total for all goals as well as an `auto sum` of the columns and  realized that the numbers did not add up unless the equal to was used `=COUNTIFS(Kickstarter!$D:$D,">=50000",Kickstarter!$F:$F,"failed",Kickstarter!$R:$R, "plays")`
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
  - Looking at the month those campaigns that were categorized as "theater" were launched we can see certain summer months had an overall larger number of campaigns both successful and failed. With the largest number of successful plays in May, June and July.  We can also see that something is happening in October with no canceled plays, but the highest number of failed plays.
-  What can you conclude about the Outcomes based on Goals?
   - Based on the chart we can see that the plays with a goal of 15000 or less or goals between 35000 to 45000 were more likely to be successful.  Plays with goals greater than 45000 had the worst success rate.
- What are some limitations of this dataset?
  - some of the limitations of this data set include the number of campaigns for plays year to year.  Looking at the data by year we see that the majority of the plays are 2014-2016 and the trends are not the same each year, or for each country.  This should warrant looking closer at the data for other subsets that may be relevant. 

- What are some other possible tables and/or graphs that we could create?
  - looking specifically at the data we have already graphed, I think it would be interesting to drill down to some of the subsets of the data.  What's really happening in those cases with a goal between 35000 and 45000?  In addition looking at data by number of backers and amount per pledge would be interesting and provide different data.  Doing a quick review it looks like 100% of the campaigns where spotlight is "true" are successful and 100% of where it is false they failed (or were canceled or are live).  This needs some looking into. 
