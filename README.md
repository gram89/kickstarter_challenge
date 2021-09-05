# Kicstarter Challenge Final Submission
## Overview of the project
**The purpose of the project was to learn excel, some basic statistics and key functions within excel to help a Crowdfunding Exercise**
The background for the project was to help Louise help launch a crowdfunding exercise by analysing data from past crowdfinding campaigns. Since she is seeking crowdfunding for a play we looked at plays as a sub-category and analysed the data to ensure that she makes an **informed, data-driven decision to launch her campaign**. Through the analysis we learned to create pivot tables and graphs which are one of the most widely used tools in any organisation.

## Analysis and Challenges
### Understanding the data
The first part of the analysis was to understand the data and one of the key things which I did here was to uncover the dates from the unicode format. This was the **first challenge** I had faced, as this date format gets used in multiple environments and coding languages and understanding what the numbers mean and uncovering the launch date and the deadline dates through the formula **_(((J2/60)/60)/24)+DATE(1970,1,1)_** was a great first step.

The second important thing I did was to colour-code the outcomes through conditional formatting. This allowed me to understand the status of every project visually and was a great help in validating future analysis at a glance. The next important aspect in understanding the data was to split the categories into parent and sub-category using the de-limiter. This furthered the understanding of data by bucketing them into relevant categories which was used in future analysis.

### Analysis:
1. **_Pivot Tables & Pivot Charts_**
  - Pivot tables were a great way to begin analysing the data which we had at hand. Clearly through the parent category and sub category pivot tables I was able to understand that plays in general have a higher tendency to be successful. However this was just the beginning and it gave me a peek into what is at stake.
2. **_Descriptive Statistics_**
  - Using descriptive statistics I was able to understand that the high fail rate is predominantly because campaigns having a higher goal than the successful campaigns in the U.S.  
 
 ![Descriptive Statistics of US campaigns](Descriptive%20Stats.png)

### Analysis of Outcomes Based on Launch Date

1. For this analysis, the first taks was to use the ***YEAR()*** function to extract only the year from the campaign launch date field. As mentioned earlier, the campiagn launch date was converted from UNICODE to readable dates using the formula **_(((J2/60)/60)/24)+DATE(1970,1,1)_**.
2. The next step was to create a pivot table with all the values and add the newly created Year column and the parent category fields as filters
3. The Launch date was set as rows and the outcomes were set as columns, the count of outcomes were set as values in the value field settings
4. The Columns were then filtered to exclude "Live" campaigns for this analysis  
![Theater Outcomes vs Launch Date](Theater_Outcomes_vs_launch.png)
5. As we can see in the above graph, Launch date plays an important role in predicting success of campaigns. Campaigns launched in May tend to have a high chance of success
### Analysis of Outcomes Based on Goals

1. Here the first task was to create the goal buckets and the columns. This was a simple copy/paste and typing exercise to get the right columns and rows
2. The next step was to use Countifs() function to extract the relevant information to populate the table. The conditions were based on goals, subcategory="Plays", and Outcomes
3. This table was further used to visualise and create the graphs
![Outcomes based on Goals](Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

While overall the exercise was easy, the new things which i learned were the conversion from **Unicode to Calendar date**. The presence of various outliers in the dataset, which skewed the results were another challenge and using descriptive statistics was helpful in uncovering this skew.

## Results

**What are two conclusions you can draw about the Outcomes based on Launch Date?**  
1. May and June are the best months to launch a theater fundraising campaign with 67% and 65% success rates respectively
2. December is the worst month to launch a theater fundraising campaign with only 48% success rate
![Successful theatre campaigns as a percentage of total campaigns in any given month](Theatre_Successful_as_percent.png)

**What can you conclude about the Outcomes based on Goals?**
1. Majority of plays have a fundraising goal of 1,000 to 4,999. Falling within this goal range will also give us a higher likelihood of success as over 72% of campaigns are successful (_second only to <1000 goals_)
2. The goal range 15,000 to 19,999 is the inflection point of the graph (_35,000 to 44,999 has too few data points and hence look like outliers_). Campaigns which have goals below 15,000 have a higher probability of success and campaigns with goals above 19,999 have a higher probability of failure.

**What are some limitations of this dataset?**
The data points are old. It shows data from 2009 to 2017. More recent data could have had a different trend. The other important limitation of the dataset was the lack of cateogry specific data. While overall the dataset had 4114 campaigns across categories, for the specific plays sub-category there were just 1066 campaigns, furhtermore only 314 plays in the U.K. which is not as robust a dataset to conduct the analysis on. 

**What are some other possible tables and/or graphs that we could create?**
1. Box and whisker plot specific to plays to understand the median and IQR and the outliers in the data
2. UK Plays based on Goals and Launch Date to understand and predict more accurately. This however will yield only 314 data points and we must exercise caution in going through this route.




