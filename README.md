# Kickstarting with Excel

## Overview of Project
### Purpose
The purpose of this analysis is to reveal trends in crowdfunding for theater projects with respect to funding campaign launch date and goals.  This analysis uses data from the popular Kickstarter crowdfunding platform.  Revealing trends that influence the success or failure of a campaign will give our client very useful insight that can be used to maximize the odds of success for their own campaign.

## Analysis and Challenges

For reference, the Excel worksheet used for the analyses described below can be found [here](./Kickstarter_Challenge.xls).

### Analysis of Outcomes Based on Launch Date

The analysis for outcomes based on launch date was performed by first aggregating the Kickstarter data such that it is organized by outcome and month of the year.  The Kickstarter data covers several years, aggregating the data by month of year is critical to determining if there are common yearly or seasonal patterns.  This aggregation was generated using an Excel Pivot Table.  Once the data was aggregated it was easy to visualize using a line graph that plots the number of each outcome type (successful, failed, and canceled) by month of year.  The result is shown below.

<figure>
<img src="resources/Theater_Outcomes_vs_Launch.png" align="center">
<figcaption align = "center"><b>Figure 1 - Plot of Kickstarter Outcomes vs. Month of Year for Theater Projects</b></figcaption>
</figure>

### Analysis of Outcomes Based on Goals
A similar process was followed to visualize outcomes based on funding goals.  The Kickstarter data was aggregated by using Excel to count every instance of a goal range.  As an example, the funding goals for successful projects that fell into the range 5000-9999 (all currencies) uses the following formula:
```
=COUNTIFS(Kickstarter!D:D, ">=5000", Kickstarter!D:D, "<10000", Kickstarter!F:F, "=successful", Kickstarter!R:R, "=plays")
```
Where column D of the Kickstarter sheet is the funding goal, column F is the outcome, and column R is the sub-category.  Once the data was aggregated the percent successful, failed, and canceled was calculated, resulting in a table of outcomes (pct) for each funding goal range.  This table is plotted in the line graph below.

<figure>
<img src="resources/Outcomes_vs_Goals.png" align="center">
<figcaption align = "center"><b>Figure 1 - Plot of Kickstarter Outcomes vs. Goals for Theater Plays</b></figcaption>
</figure>

### Challenges and Difficulties Encountered
A key challenge when working with Excel is formula readability.  Long formulas on a single line of text can be difficult to read and troubleshoot if a mistake is made when entering that formula. To manage this I often build up the formulas incrementally and confirming it is doing what I expect with every increment.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

???? The first conclusion we can draw from the Outcomes based on Launch Date is that the outcome is generally not affected by launch date unless it is launched in December (maybe, the pct success is higher in spring but number of failures/cancels is flat).   number  of failures and cancellations is relatively flat throughout the year and the total number of campaign launched

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
