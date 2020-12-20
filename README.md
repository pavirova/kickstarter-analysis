# Kickstarting with Excel

## Overview of Project

### Purpose
The purpose of this analysis consists of finding trends in a dataset composed of different types of campaigns that Louise has worked on in order to draw informed conclusions and answer questions that could help Louise promote her campaigns better in the future. After seeing how quickly her play, *Fever* came close to its fundraising goal, Louise wants to understand how different campaigns performed in terms of their launch dates and fudnraising goals. This analysis will help answer how the different campaigns performed.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
To analyze the outocmes of campaigns based on their launch date, the year the campagin started was extracted from the "Date Created Coversion" column using Excel's YEAR() function. Then, a pivot table was created on the *"Theater Outcomes by Launch Date"* sheet to help better understand the number of successful, failed, and canceled campaigns based on the month in which they were launched. Once the pivot table was sorted correctly and filtered to show only data for campaigns in the theater parent category, a line chart was created to better illustrate any trends between the campaign outcomes and the months in which they were launched. Below is the **Theater Outcomes Based on Launch Date** line chart.

![Theater_Outcomes_vs_Launch](/Users/PaolaRomero/Desktop/UT Bootcamp/Bootcamp Projects/Activity 1 Crowdfunding Campaign/Challenge 1/resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
To analyze the outcomes of campaigns based on their required goals, the "Outcomes Based on Goals" sheet was created. In the sheet, dollar-amount ranges were created under the "Goal" column to group campaign outcomes based on the goal amount ranges in which they fall. Additional columns were created to analyze the number of successful, failed, and canceled projecs by goal range. To populate the mentioned columns, Excel's COUNTIFS() function was used to count the numnber of "successful", "failed" and "canceled" campaign projects depending on the goal amount range being populated, so long as the projects being counted are specifically found in the "plays" subcategory. Next, the total number of successful, failed, and canceled projects per goal range were added together using Excel's SUM() function. 

Once the total projects by goal range were added, the percentage of successful, failed, and canceled projects were calculated in relation to the total number of projects by dividing the "Number Successful", "Number Failed", and "Number Canceled" columns by the "Total Projects" column. To better illustrate any trends between the outcomes of projects in relation to the goal amount needed per project, the **Outcomes Based on Goal** line chart was created.

![Outcomes_vs_Goals](/Users/PaolaRomero/Desktop/UT Bootcamp/Bootcamp Projects/Activity 1 Crowdfunding Campaign/Challenge 1/resources/Outcomes_vs_Goals.png)


### Challenges and Difficulties Encountered
During this analysis, I encountered a challenge when writing out Excel's COUNTIF() function. When I ininitially wrote out the formula, Excel said there was an error and the formula was not calculating. To overcome this, I watched the video provided on the Challenge module that walks through how to properly use the COUNTIFS() function. I realized then that my formula was not calculating because I had not put quotation marks around the criteria that the function needed to follow. Once I went back and applied parenthesis to each of the criteria, the formula worked properly. It is important to ensure that the correct syntax is used when writing Excel formulas to ensure calculations perform correctly.
 
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
From analyzing the **Theater Outcomes Based on Launch Date** chart, a conclusion that can be drawn is that May is the month where most theater campaigns have successful outcomes. Additionally, we can also conclude that the number of theater campaigns that are cancelled remains relatively low and constant regardless of the month of the year in which the campaign was launched, with the exception of January, which is the month with the highest number of canceled campaign outcomes.

- What can you conclude about the Outcomes based on Goals?
From analyzing the **Outcomes Based on Goal** chart, a conclusion that can be drawn is that the highest percentage of successful outcomes (76%) occurs in campaigns with goals of dollar-amounts less than 1,000.

- What are some limitations of this dataset?
A limitation of the kickstarter dataset is that there are many different types of campaigns with different parent categories and subcategories held at different time lengths. For example, one play's campaign might last a month, while a television show's campaign could last three months. Becuase there are different time lengths for how long each campaign lasts, only looking at the successful, failed and canceled outcomes per month does not give completely reliable data, since a variable that should also be taken into account is the length of the duration of each campaign. Then, if we wanted to, we could see if there are any trends found when comparing campaign length to ouctome, as campaigns with longer duration periods are likely to increasew their success if people have more time to provide funding to a particular campaign. 
Additionally, another limitation of the dataset is that different people with different personal preferences are donating to different campaigns depending on what country the campaign is taking place. The sample size of the people donating funds to the different campaigns is not the same throughout, it changes depending on the country in which the campaign is taking place. The market for the different parent categories and subcategories of the campaigns should be researched by country as this is something that could be skewing results a certain way and thus limiting our analysis. For example, if the market for television shows is better than the market for plays in Great Britain, the television campaigns are more likely to have a higher outcome of success. The performance of the different campaigns could vary based on the market for it on the country in which it is taking place.

- What are some other possible tables and/or graphs that we could create?
Another table that could be created is a table that includes a column where the duration of each campaign is calculated in days based on the start and end dates. Once the number of days per campaign is calculated, we could get a better representation on campaign outcomes by campaign length. To better illustrate any trends between campaign lengths and outcomes, we could group the campaign lengths in different ranges of duration days and create a bar graph showing the number of successful, failed, and canceled outcomes based on the different campaign duration ranges. Additionally, we could create pie graphs to show the different percentages of successful, failed, and canceled outcomes for each of the different goal dollar-amount ranges.
