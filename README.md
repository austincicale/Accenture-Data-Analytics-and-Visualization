# Accenture Data Analytics and Visualization

### Project Overview

This project is a Data Analytics and Visualization job simulation offered through Forage, a platform providing free virtual work experience that replicates daily tasks at top companies. In this simulation, I assumed the role of an analyst working for Accenture. My task was to assist Social Buzz, a fictional social media company experiencing rapid growth, in implementing best practices for handling large datasets. Specifically, I analyzed their content categories to identify the top 5 categories with the highest aggregate popularity.

### Requirements gathering
The key objectives, tasks, and data consideration are outlined below:

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

  1. **Reaction**: Contains data on all reactions to content, including *Content ID*, *Reaction Type*, and *Datetime*.
  2. **Content**: Provides information about all posts, including *Content ID* and *Content Category*.
  3. **Reaction Types**: Describes *Reaction Type* and their associated *Reaction Score*.

- #### Approach
  To determine the popularity of different content categories, the analysis involves aggregating the reaction scores for each category. Therefore, it is essential for the *Content Category* and *Reaction Score* variables to be in the same data set. This can be achieved by merging the three selected data sets by common variables.  

### Data Cleaning
The following steps were taken during the data-cleaning process:

- #### Step 1: Removing Irrelevant Columns
  Variables removed from the following datasets:
  
   - **Reaction**: *User ID*
   - **Content**: *User ID*, *URL*

- #### Step 2: Handling Missing Values
  Observations with missing values were removed from the datasets. This was achieved using Excel's Filter tool, allowing for efficient identification and removal of rows containing missing data.

- #### Step 3: Addressing Duplicates
  Upon examining the unique *Content Categories* in the **Content** dataset, it was discovered that some observations contained quotation marks, leading to duplicate entries. To address this issue, the Replace tool in Excel was utilized to remove all quotation marks.

### Data Modeling
The following steps were undertaken to identify the top 5 content categories and conduct any additional analysis:

- #### Data Merging

- Top 5 Content Category Identification

- Further Analysis
Now we want to figure out the top 5 categories. To complete your data modelling, follow these steps:

1. Create a final data set by merging your three tables together

We recommend using the Reaction table as your base table, then first join the relevant columns from your Content data set, and then the Reaction Types data set.
Hint: You can use a “VLookUp” formula
 
2. Figure out the Top 5 performing categories

Add up the total scores for each category.
Hint: You can use the “Sum If” formula

The end result should be one spreadsheet which contains:

A cleaned dataset
The top 5 categories

