# Kickstarting with Excel

## Overview of Project

### Purpose

The purpose of this project is to visualize data to help Louise see how different campaigns fared in relation to their launch dates and their funding goals. Louise can then use that data to determine their own start date and goal for her campaign to maximize success. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

This analysis was performed by creating a [pivot table](./resources/Outcomes_by_Launch_Date_table.png) using the Kickstarted data filtered by the "theater" category and then creating a [line chart](./resources/Theater_Outcomes_vs_Launch.png) to help visualize the data. I also went ahead and created an [additional line chart](./resources/total_theater_productions_by_launch_date.png) that shows the total number of theater productions by launch date regardless of outcome. Then I found the percentage of successful campaigns relative to each months total, and then found the difference of that total and the average across all months to find the likelyhood of success regardless of number of total campaigns. I then charted that data with a [line chart](./resources/difference_of_%25successful_by_month_to_average.png) as well, which also shows a positive correlation with total campains and with successful campaigns. 

### Analysis of Outcomes Based on Goals

This analysis was performed by making a [table](./resources/Outcomes_by_Launch_Date_table.png) in excel that grouped different bins of goal amounts on each row. Then for each number of successful, failed, or canceled projects, I used a =countifs() function that counted the number of projects in each of those categories. The total projects was calculated using a simple =sum() function, and the percentage columns were performed by using a simple "/" operation on the relevant cells. 

### Challenges and Difficulties Encountered

One challenge that I had was the number of subcategory plays (not parent category theater) that were canceled in this dataset. I saw that the number of canceled plays was 0 and I assumed this was an error on my part, but it turns out that there were indeed 0 canceled plays in this dataset. I figured that since the requirements of the challenge included finding the number of canceled plays that the number should certainly be >0, and I spent a good chunk of time trying to figure out where I went wrong before confirming this was the expected outcome. 
Another challenge I had was trying to create a table in the "Outcomes by Launch Date" sheet that showed the total number of theater productions regardless of outcome. I couldn't figure out how to get just the Grand Total for each month to show up on a line chart. I used a workaround using the =getpivotdata() function to create additional columns that were not part of the pivot table and charted those instead. I then realized it could have been achieved by copy and pasting. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
    - The most obvious conclusion found in the data was that a launch date in May has the highest number of successful theater productions kickstarters followed by a downward trend for the remainder of the year, excluding a slight bump in number in October. We can use this information to determine the optimal time for launching a campaign is May. 
    - Another conclusion that we can make about this data is that the number of successful campaigns is directly correlated with the total number of campaigns. In my own "off the book" analysis, I found that May is still the best month to launch a campaign with a 5.58% greater chance of success compared to the average and that December is by car the least best with an 11.95% likelyhood of failing or being canceled. I also found this data to be positively correlated with total number of campaigns as well as just successful campaigns.

- What can you conclude about the Outcomes based on Goals?
    - We can conclude that the smaller the goal amount, the more chance there is for success. The exeption is in the $35,000 to $45,000 range, but that can be explained by the low number of campaigns with those goal amounts where a couple of small datapoints can skew the results.
    - The other conclusion we should draw is that a >$45,000 goal is highly unlikely to succeed. Out of 15 campaigns to fit that criteria, only two were successful.

- What are some limitations of this dataset?
    - One limitation of this data, that I have attempted to correct for in the "outcomes by launch date" section, is that the required charts and tables do not account for total number of campaigns and how that effects the chances of success or failure. 
    - Another limitation of this dataset is it does not account for how plays and other theater productions fare when compared to other categories of kickstarters, such as tech or fashion. The conclusion of "May is the best month to start a campaign" can be negated by the economic situation of the donors on that specific year. One possible explanation for May being the best month to start a campaign can be explained by USA campaign donors receiving their tax returns in April and using that money in May for charitable tax writeoffs. This dataset only accounts for numbers without regard to external influencers. 

- What are some other possible tables and/or graphs that we could create?
    - I went ahead and did this, but charting the total number of campaigns, finding the percentage of successful campaigns, and comparing that to the average chances of success. 
    - Another comparison we could create is how theater and play productions fare against other categories and subcategories of campaigns in the same launch dates and goal tiers. 
