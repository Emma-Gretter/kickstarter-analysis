# Kickstarting with Excel

## Overview of Project
This project used Kickstarter data from campaigns launched between 2010-2017, from various countries, with goals amounts between $1 and $100 million, and various campaign lengths, to determine success rates of certain campaign parameters. 

### Purpose
The purpose of this project is to compare your campaign to similar campaigns to determine which campaign parameters will be most successful for your project. 

## Analysis and Challenges


### Analysis of Outcomes Based on Launch Date
For this analysis I first pulled the data for all successful, failed, and canceled campaigns. I compared the number of each type of campaign that was started in each month of the year by creating a pivot table as seen below. 

![PivotTableLaunch](https://github.com/Emmagrace878/kickstarter-analysis/blob/main/Resources/PivotTableLaunch.png)

Using the pivot table, I created a line graph (as seen in [“resources”]( https://github.com/Emmagrace878/kickstarter-analysis/tree/main/Resources) 
) 


### Analysis of Outcomes Based on Goals
For this analysis I first pulled data for each successful, failed, and canceled campaign based on the range of the goal amount. I used COUNTIFS functions such as the one below to show how many of each type of campaign had a goal amount within the given range. 

```
=COUNTIFS(Kickstarter!F:F,"Successful",Kickstarter!D:D,"<1000",Kickstarter!R:R,"plays")
```

I then used ROUND functions such as the one below to calculate the percentage of all projects that were successful, the percentage that failed, and the percentage that was canceled. 

```
=ROUND(B2/E2*100,2)
```

I then created a pivot table, as seen below. 

![Pivot_Table_Goals]( https://github.com/Emmagrace878/kickstarter-analysis/blob/main/Resources/Pivot_Table_Goals.png)

Using the pivot table, I created the line graph (as seen in [“resources”]( https://github.com/Emmagrace878/kickstarter-analysis/tree/main/Resources))

### Challenges and Difficulties Encountered

A challenge I encountered was the combination of numbers and letters in the pivot table for the “outcomes based on goals” analysis. When creating my line graph the values were out of order since “Greater than 50000” and “Less than 1000” automatically fell to the bottom of the list. 

![Challenge.PivotTable.Goals]( https://github.com/Emmagrace878/kickstarter-analysis/blob/main/Resources/Challenge.PivotTable.Goals.png)

I was able to correct this issue, and my corresponding graph, by clicking and dragging the values to their correct location. Once the values were in the proper order the graph protrayed the correct inforamtion. 

![Pivot_Table_Goals]( https://github.com/Emmagrace878/kickstarter-analysis/blob/main/Resources/Pivot_Table_Goals.png)
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

  * June is the best month to launch a theater Kickstarter campaign.
  * December is the worst month to launch a theater Kickstarter campaign. 


- What can you conclude about the Outcomes based on Goals?

  * Campaigns with a goal of less than $1,000 are most likely to be successful. 

- What are some limitations of this dataset?

  * This dataset does not tell us how much was spent on each campaign such as, campaign video production costs.
  * This data set does not tell us the types of rewards offered to donors. 


- What are some other possible tables and/or graphs that we could create?
  * We could create a table illustrating the impact of “staff pick” status on campaign success. 
  * We could create a bar graph showing “length of campaign” as x-axis and “total pledged” as y-axis to determine if longer campaigns equal greater      amount of donations.  
![image](https://user-images.githubusercontent.com/84678564/122684229-6e0a6380-d1c1-11eb-8dd4-008104714dd4.png)
