# Kickstarter-Analysis 


## Overview of Project

The objective of the project was to use past kickstarter campaign data to analyze and assess how previous campaigns fared according to specific factors like 'launch dates' and 'funding goals'.

### Purpose

The purpose was to get some insight into how the above mentioned two factors influence the likelihood of a campaign being a success or failure and in some cases, getting cancelled, and whether there are any patterns to be found. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

The first major part of the analysis was to get some more information about the outcomes of campaigns based on launch dates. The plan was to create a pivot table and an accompanying chart focused on the pertaining variables and factors. A new sheet 'Theatre Outcomes by Launch Date' was created to present the results for this section. On the main worksheet, 'Kickstarter_Challenge', there was a need to create a new column with 'years' for all launch dates. This was done by using the YEARS() function on the 'Date created conversion' column. 

The 'Years' column would be used as a filter along with 'Parent category' for the pivot table. The rows had 'Date created conversion' and the columns had 'Outcomes'. The sum values were 'Count of outcomes'. This pivot table was named 'Theatre Outcomes by Launch Date'. Finally, the 'Parent category' was filtered to show data for 'Theatre' only. For easy visualization, an accompanying line chart was created from the pivot table. The 'Theatre_Outcomes_Vs_Launch.png' chart is embedded below.

![Theatre_Outcomes_vs_Launch](https://user-images.githubusercontent.com/92544151/148625901-1c8882ae-beac-49a5-8854-2eaf097ebeff.png)

### Analysis of Outcomes Based on Goals

A new worksheet was created for this section, 'Outcomes Based on Goals'. The following table was created to obtain more detailed information on project goals and the success, failure or cancelled ratio. 

<img width="993" alt="Outcomes_Vs_Goals_Table" src="https://user-images.githubusercontent.com/92544151/148626218-81c1492a-9312-49bb-aea5-c820e9ef1ce4.png">

To generate the table efficiently, the COUNTIFS() function was used to populate the number of successful, failed and canceled projects. SUM() was utilized for the 'Total Projects'. Percentages were calculated and rounded to 2 decimal places. Then, a line chart, 'Outcomes_Vs_Goals.png', was created for visualization. 

![Outcomes_Vs_Goals](https://user-images.githubusercontent.com/92544151/148625927-2e857101-6f18-4cb3-b925-6095b77707eb.png)

### Challenges and Difficulties Encountered

There were no significant difficulties encountered during the project but given that fact that it was my first time working with COUNTIFS(), it took me slightly longer than expected getting the information tabulated in 'Outcomes Based on Goals'. 

When creating the pivot table for 'Theatre Outcomes for Launch Date', it was important to focus on rows. One could encounter some difficulty if they used 'Date created conversion column' for rows in the pivot table, as this would lead Excel to create extra categorization items. 

## Results

The results section of this report will be focusing on the following four major questions:

- What are two conclusions you can draw about the Outcomes based on Launch Date?

When looking at the 'Theatre Outcomes by Launch Date' worksheet, it is easy to draw some conclusions. The month of May had the highest number of successful and failed campaigns when compared to the rest of the year. This could be due to the fact that more theatre campaigns are launched in May (166) when compared to other months but given the exaggerated jump in the percentage of successful campaigns, it can be said that May is the best month to launch a campaign. It is also clear that majority of the theatre campaigns were successful, regardless of the month. 61.3% of total theatre campaigns were successful. 

On the other hand, it is easy to see the drop in the number of successful campaigns for December. The total of failed and canceled campaigns (35 + 3) for the month is greater than the number of successful campaigns (37). This makes December the only month with less than a 50% success rate. Needless to say, avoid launching campaigns in December.  

- What can you conclude about the Outcomes based on Goals?

The percentage of cancelled campaigns was zero, so the chart clearly shows the inverse pattern between percentage successful and percentage failed, as one would expect. Also highlighted by the table is the fact that the highest percentages of the successful campaigns take place when the goals are around the lowest ranges. Even though it appears that '35000 to 39999' and '40000 to 44999' ranges have comparatively high percentage successful numbers, it should be noted that the sample size is not big enough for those ranges. Both ranges combined have 9 total projects so the results can be skewed. The top 4 lowest ranges though tend to have the most total projects and greater than 50% success rate.  

- What are some limitations of this dataset?

Looking at the dataset, the latest information about project comes from the year 2017. It needs to be updated to incorporate the changes over the past two years, especially when considering the global pandemic. The pandemic is bound to have had some definitive impact on the funding for these projects. Someone looking at the data today and trying to gain insight about how to start their own campaign would be amiss not to take the pandemic into account. 

It is also important to note that there are other factors involved in the success of a campaign. How is a campaign proposed or advertised to the people? Is it a single person behind the project or is it a team that has a proven track record when venturing in this field? Let's say there are two projects with a $15000 funding goal each and getting launched on the same day. Project A is being launched by an indie company that just had a successful play come out last year. Project B, on the other hand, is being proposed by a single passionate person. Even though both of them have the same goals, it is much easier to envision project A being a success rather than project B. 

- What are some other possible tables and/or graphs that we could create?

As mentioned, it would be helpful to have data about who is behind the project and whether it's an indie company or a single individual. Along the same lines, creating a pivot table to see how each one (single individual or a team) impacts the success of the campaigns.

Data about the campaign creators' past record with regards to past campaigns might be helpful too. If someone has had multiple successful campaigns in the past, it's easy to see them have another one. So, a pivot table and accompanying chart representing and comparing this information might be helpful when trying to draw conclusions from the dataset.  
