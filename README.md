# Data Analysis with Excel on Crowdfunding Dataset
## Overview of Project
Louise is a playwright who has written a new play called, "Fever". She wants to launch a crowdfunding campaign to fund her play in the United States and estimates that the play's budget would be $10,000. The aim of this data analysis is to uncover invaluable information that can help our client Louise decide whether she will be able to successfully launch a crowdfunding campaign to fund her play.
### Purpose
Analysis is done with Excel on the crowdfunding dataset that contains information on goal and pledged campaign amounts, campaign status divided geographically, and by categories. Louise wants to know if there are specific factors that can make the project campaign successful. 

### Analysis of Outcomes Based on Launch Date

![Theatre_Outcomes_vs_Launch](https://user-images.githubusercontent.com/75961057/138757504-5047b119-89c2-449a-be61-e027000c56c0.png)
![image](https://user-images.githubusercontent.com/75961057/138769008-aa8cd609-e681-4724-a239-f12d3d47f7aa.png)

Using Pivot Tables, we can summarize the number of successful, failed and canceled campaigns for the category "theatre" filtered by month and year. From the chart and table above you can see that there is clear spike in successful campaigns in May (111 successful campaigns) and June (100 successful campaigns) when compared to the number of failed campaigns (52 in May and 49 in June). 

### Analysis of Outcomes Based on Goals

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/75961057/138758021-e3ad0e8a-2573-481e-93b0-dd13519650ce.png)
![image](https://user-images.githubusercontent.com/75961057/138770227-0ec451b1-e499-4fab-89d8-be963e8e0e67.png)
This is a calculation of the number of successful/failed/canceled campaigns corresponding to the goal amount range for the category 'theatre" and subcategory "plays". The number of successful campaigns seem to decrease with increasing goal amaounts. The exception is at $35,000-$45,000 but the data points are too few to make a definitive conclusion at this point. However, you can see that the number of successful campaigns increase below $5000 and the rate of success is ~75%. 

### Challenges and Difficulties Encountered
There were no significant challenges encountered with this dataset. 
1. Understanding what story the data was saying and identifying and modifying the columns according to project requirements was challenging. +
2. During data cleaning, Columns I(deadline) and J(launched_at) in the dataset were in UNIX datastamp format. They had to be converted to Date/Month/Year (eg: 3-Mar-16) format and were stored in columns S(Date Created Conversion) and Column T(Date Ended Converstion) for readability. Having not worked with Unix timestamps, this while not challenging was a new concept to learn.

## Results

#### What are two conclusions you can draw about the Outcomes based on Launch Date?
1. Louise should plan her campaigns in the months of May and June for it to have a chance of a successful campaign. May and June also are the months when there are maximum number of campaigns. 
2. The data shows that almost all the campaigns in the month of December has failed. Louise should avoid launching a campaign in the month of December. 

#### What can you conclude about the Outcomes based on Goals?
Louise will have ~75% chance of a successful campaign if she keeps her goal below $5000. There is only a ~50% chance that she can achieve her original goal of raising $10,000

#### What are some limitations of this dataset?
1. There are not significant number of data points for campaigns with higher goal amounts. This makes the analysis slightly skewed towards campaigns with lower goal amounts. 
2. We see that while it is possible to say that campaigns under $5000 are ~75% successful, since the median pledged amounts for failed campaigns are much lower than for successful campaigns, there could be other reasons due to which the campaigns failed other than the goal amounts which is not provided in the dataset. 

#### What are some other possible tables and/or graphs that we could create?
##### 1. Statistics Table 
This Table shows the Mean, Median, Mode, Standard Deviation and Quartiles. This table would tell us how far the data is spread about the mean, where we can look for outliers so that Louise can eliminate data points not relevant to her needs. 
![image](https://user-images.githubusercontent.com/75961057/138793226-64b7fcbf-f1f0-4abe-83ee-1dead6b9f5ed.png)

The table tells us that since the mean and median of the pledged amounts are much lower for failed campaigns as compared to the successful campaigns who have exceeded their goal amounts by ~$600. The Failed campaigns also have a much higher Mean indicating as we did from the Outcomes Based on Goals table/chart, that higher goals campaign fail more than campaigns that are lower than $5000. This strengthens our previous analysis. We can also see that the outliers are campaigns in USA over ~$10,000 
 
##### 2. Histogram of Successful and Failed Goal Outcomes of Campaigns in USA to strengthen our finding. 
 ![image](https://user-images.githubusercontent.com/75961057/138794104-0b5cd532-ec86-4604-a1c4-6c2d961bba6e.png)
  ![image](https://user-images.githubusercontent.com/75961057/138797625-46f948be-8611-42c4-aacd-740369834e76.png)
  
 Now that we know from Outcomes based on Goals for "Theatre/Plays" category for the entire dataset, it would be useful to see if same criteria specfic to USA would also show similar trend as Louise wants the play to be in USA. We see most successful campaigns are below $5000 in USA too. 
