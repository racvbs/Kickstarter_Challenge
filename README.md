# Kickstarter_Challenge
Module 1 Challenge
## Overview of Project
### Background
Louise’s play Fever came close to its fundraising goal in a short amount of time. Now, she wants to know how different campaigns fared in relation to their launch dates and their funding goals. We have the Kickstarter dataset where are visualized campaign outcomes based on their launch dates and their funding goals.

### Purpose
The objective of this analysis is to make the best decisions about campaings for her play. 
### Information
Even Louise has many information on the table Kickstarted, we need to organize the data in order to know key numbers and be able to have an strategy.
We have many variables, but I consider these 4 as principal to be analysed: campaingn' **Category/Subcategory**, launch **Month**, campaing **Outcome** and campaing **Goal**.
With these 4 variables we are able to analyse the basics:
> If the launch month impact to outcome of the campaing, and if it does we need to know the best months to lanch.
> 
> If there's a relationship between the campaing outcome and the goal amount. 

*Note: The variable **Category/Subcategory** is used to filter only "theater" and "plays" campaings and it was splitted from the original to make **Category** and **Subcategory** variables*
## Analysis and Challenges
To fullfille our strategy need and, as I mentioned before, there are two analysis in this paper:
1. Outcomes based on lauch date
2. Outcomes based on goals
### Analysis of Outcomes Based on Launch Date
The campaing outcomes were organized by launch month from the past 9 years (2009-2017), filtered by campaings lunched on theaters.

This table gives kew information to know which months are better than others and if the data has a trend through the year.
In order to visualize better this information, there is a graphic that explains it.
![Theater Outcomes by Launch Date](https://user-images.githubusercontent.com/85086918/123524268-b7115a80-d68e-11eb-81f8-58e6a5ec4ead.png)

**Conclusion:**

**1. The best month to launch a campaing in theathers is May, from there, the campaigns are likely to fail as the months go by.**

**2. There is a bigger chance to fail On October.**
```
Technical Notes:
- Dates were change from Unix to Excel readable timestamp.
- Months were defined with "=month(launched_at)" formula and converted to qualitative month names.
- Category/Subcategory variable was splitted in two variables with Text to columns feature
- The table for this analysis was made as a Pivot Table
  - Filtered by Parent Category "theater"
  - Filtered by Year
  - Rows by Month
  - Columns by outcome avoiding live campaings
```
### Analysis of Outcomes Based on Goals
The analysis of outcomes by goals is important to know how risky is to increase goals and the ranges to do it.

The filter by "plays" was made and the goal variable was ranged by Less than 1,000, each 5,000 until more than 50,000.
The graphic is this:

![Outcomes Based on Goals](https://user-images.githubusercontent.com/85086918/123524421-c04ef700-d68f-11eb-81d4-1e27ab6a65fe.png)

**Conclusion: The bigger the goal the campaigns are more likely to fail**
Although it seems that in the range of 35,000 to 45,000 there is more probability of being successful, the number of campaigns is not enough to conclude this.
```
Technical Notes:
- Ranges for goals were distributed homogeneously:
  - Less than 1,000
  - 1,000 to 4,999
  - 5,000 to 9,999
  - 10,000 to 14,999
  - 15,000 to 19,999
  - 20,000 to 24,999
  - 25,000 to 29,999
  - 30,000 to 34,999
  - 35,000 to 39,999
  - 40,000 to 44,999
  - 45,000 to 49,999
  - Greather than 50,000
- To count the number of registers the formula "=countifs" was used with 3 criteria:
  - Outcome
  - Goul range
  - Subcategory "plays"
```
### Challenges
The big challenge in any analysis is to have clean data. This time everything was clean and clear and the date transformation was very easy.
I think this excersise was quite good.

## Results
Summarizing
*What are two conclusions you can draw about the Theater Outcomes by Launch Date?*

**1. The best month to launch a campaing in theathers is May, from there, the campaigns are likely to fail as the months go by.**

**2. There is a bigger chance to fail On October.**

*What can you conclude about the Outcomes based on Goals?*

**The bigger the goal the campaigns are more likely to fail**

*What are some limitations of this dataset?*

**The data doesn't have location, timimg of set up, expenses, duration or number of people involved in campaings, so our conclusions doesn't have context.
Also we need external variables to understand the situation of plays in general, competetitors, etc.**

*What are some other possible tables and/or graphs that we could create?*

**In this table are many options:**
- Outcome by Country or Currency
- Outcome by Bakers
- Outcome by Staff_pick
- Outcome by percentage of pledge
- Even all of them by year, or by goal range, among other
Neverless the context of analysis give us the way to go and the questions to solve.


By Raquel Valdez
