# Accenture Data Analytics and Visualization

### Project Overview

This project is a Data Analytics and Visualization job simulation offered through [Forage](https://www.theforage.com/), a platform providing free virtual work experience that replicates daily tasks at top companies. In this simulation, I assumed the role of an analyst working for [Accenture](https://www.accenture.com/us-en?c=acn_glb_sembrandpuregoogle_13513493&n=psgs_0323&&c=ad_usadfy17_10000001&n=psgs_Brand-%7C-US-%7C-Exact_accenture&gad_source=1&gclid=CjwKCAjw8diwBhAbEiwA7i_sJeiI6Y78t8x7NfmFfNG29AQ7htWfyyP2V5E19Fo-96jXWMkeu-Z4BhoC65IQAvD_BwE&gclsrc=aw.ds). My task was to assist Social Buzz, a fictional social media company experiencing rapid growth, in implementing best practices for handling large datasets. Specifically, I analyzed their content categories to identify the top 5 categories with the highest aggregate popularity.

### Requirements gathering
The key objectives, tasks, and data considerations are outlined below:

- #### Business Problem 
  The client, Social Buzz, has experienced significant growth but lacks internal resources to manage the scale effectively. Accenture has been   tasked with addressing the following key objectives:

  1. Conduct an audit of Social Buzz's big data practices.
  2. Provide recommendations for an IPO.
  3. Perform an analysis of popular content to better understand audience preferences.

- #### Personal Task as Data Analyst 
  - Analyze sample datasets provided by Social Buzz and generate visualizations to identify the most popular content categories.
  - The goal is to determine the top 5 categories with the highest popularity based on reaction scores.

- #### Data Sets
  I was provided with 7 datasets, each containing different columns and values. The initial step involved identifying the necessary datasets to complete the task effectively. Given that popularity is determined by reaction scores, the following datasets were selected:

  1. [Reactions](Reactions.csv): Contains data on all reactions to content, including *Content ID*, *Reaction Type*, and *Datetime*.
  2. [Content](Content.csv): Provides information about all posts, including *Content ID* and *Content Category*.
  3. [Reaction Types](ReactionTypes.csv): Describes *Reaction Type* and their associated *Reaction Score*.

- #### Approach
  To determine the popularity of different content categories, the analysis involves aggregating the reaction scores for each category. Therefore, it is essential for the *Content Category* and *Reaction Score* variables to be in the same data set. This can be achieved by merging the three selected data sets by common variables.  

### Data Cleaning
The following steps were taken during the data-cleaning process:

- #### Step 1: Removing Irrelevant Columns
  Variables removed from the following datasets:
  

    | Dataset       | Removed Variables                                                                          |
    |---------------|-------------------------------------------------------------------------------|
    | Reactions         | User ID                                               |
    | Content       | User ID, URL                                         |


- #### Step 2: Handling Missing Values
  Observations with missing values were removed from the datasets. This was achieved using Excel's "Filter" tool, allowing for efficient identification and removal of rows containing missing data.

- #### Step 3: Addressing Duplicates
  Upon examining the unique *Content Categories* in the **Content** dataset, it was discovered that some observations contained quotation marks, leading to duplicate entries. To address this issue, the "Replace" tool in Excel was utilized to remove all quotation marks.

### Data Modeling
The following steps were undertaken to identify the top 5 content categories and conduct any additional analysis:

- #### Data Merging
  Attributing the **Reactions** dataset as the base table, Excel's "VLOOKUP" formula was used to execute the following merges:
  - Using *Content ID* as the "lookup_value", *Content Type* and *Content Category* were merged from the **Content** dataset to the **Reactions** dataset.
  - Using *Reaction Type* as the "lookup_value", *Reaction Sentiment* and *Reaction Score* were merged from the **Reaction Types** dataset to the **Reactions** dataset.
  
  After merging the three data tables, we have our [final data set](FinalData.xlsx) and can identify the most popular content categories. 
  
- #### Top 5 Content Categories

  After copying all content category observations into a new Excel tab, a discrete list of the categories was obtained using Excel's "Remove Duplicates" tool. For each unique category, the "SUMIF" function was used to accumulate reaction scores among all observations from the cleaned data set. Once the aggregate reaction scores were established for each content category, the list of categories was sorted in descending order to identify the top 5 most popular. Below are the top 5 categories, accompanied by a bar chart illustrating the total reaction scores for all content categories.

  ##### 1. Animals
  ##### 2. Science
  ##### 3. Healthy Eating
  ##### 4. Technology
  ##### 5. Food

  #### *Total Reaction Scores by Category*
  
  <img width="505" alt="Screenshot 2024-04-11 at 9 13 03 PM"   src="https://github.com/austincicale/Accenture_Data_Analytics_and_Visualization/assets/77798880/c8edb421-dd4a-4772-bded-53a34d4d53c2">

- #### Further Analysis

  In addition to assessing the popularity of content categories, I conducted an analysis on the popularity of reaction types. Similarly, I compiled all reaction type observations into a new Excel tab and generated a distinct list of reaction types using the 'Remove Duplicates' tool. For each unique reaction type, I employed the 'COUNTIF' function across all observations in the cleaned dataset to determine the frequency of each reaction type's occurrence. Below are the top 5 most popular reaction types, along with a bar chart illustrating their respective frequencies. 

  - #### Top 5 Reaction Types: 
    ##### 1. Heart
    ##### 2. Scared
    ##### 3. Peeking
    ##### 4. Hate
    ##### 5. Interested

    #### *Reaction Type Count*

    <img width="635" alt="Screenshot 2024-04-11 at 9 13 41 PM" src="https://github.com/austincicale/Accenture_Data_Analytics_and_Visualization/assets/77798880/e24a20ce-c54a-4af7-a93a-fb4a42996c00">

  My final analysis aimed to identify the most popular months based on the frequency of posts. In the final dataset, the *Datetime* variable signifies the timestamp of each post. To facilitate analysis, I created a new column in Excel using the "TEXT" function to extract the month from each *Datetime* observation. Subsequently, I generated a list of each distinct month in a new Excel. Utilizing the newly created column containing only the months extracted from the *Datetime* varriable, I used the "COUNTIF" function to tally the number of posts for each month. Below are the top 5 months with the highest post count, accompanied by a visualization illustrating the distribution of posts across each month.
    

  - #### Top 5 Months:
    ##### 1. May
    ##### 2. January
    ##### 3. August
    ##### 4. December
    ##### 5. July

    #### *Number of Posts by Month*

    <img width="517" alt="Screenshot 2024-04-11 at 9 14 14 PM" src="https://github.com/austincicale/Accenture_Data_Analytics_and_Visualization/assets/77798880/f02891c8-879f-462f-9198-bde22a607f72">

### Presentation

After completing all my data analysis tasks, I was advised to create a presentation that would hypothetically be presented to the team at Social Buzz, highlighting the process of my analysis and key insights that were uncovered. My presentation can be found [here](AccentureJobSim.pptx).
