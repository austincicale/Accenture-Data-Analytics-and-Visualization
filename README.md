# Accenture Data Analytics and Visualization

### Project Overview

This project serves as a simulated Data Analytics and Visualization job experience offered through Forage, a platform providing free virtual work experience programs. In this simulation, I assumed the role of an analyst working for Accenture. My task was to assist Social Buzz, a fictional social media company experiencing rapid growth, in implementing best practices for handling large datasets. Specifically, I analyzed their content categories to identify the top 5 categories with the highest aggregate popularity.

This project 
Accenture's Data Analytics and Visualization Job Simulation, offered through Forage

Social Buzz

### Requirements gathering

Business Problem: The client has reached a massive scale within recent years and does not have the resources internally to handle it. Accenture is tasked to fulfill the following: Audit of big data practice, recommendations for IPO, analysis of popular content

Personal task as a data analyst: Analysis of sample data sets with visualizations to understand the popularity of different content categories

Provided with 7 data sets, each containing different columns and values

So, the first step is to use this data model to identify which datasets will be required to answer your business question - which is to to figure out the top 5 categories with the largest popularity.
Your job is to identify which content categories are most popular. Popularity is determined based on reaction scores.
Decided to use the following data sets: Reaction, Content, Content Types

The brief carefully it states that the client wanted to see “An analysis of their content categories showing the top 5 categories with the largest popularity”.
As explained in the data model, popularity is quantified by the “Score” given to each reaction type.
We therefore need data showing the content ID, category, content type, reaction type, and reaction score.
So, to figure out popularity, we’ll have to add up which content categories have the largest score.

### Data cleaning

First, Open the three selected data sets

Clean the data by:

removing rows that have values which are missing,
changing the data type of some values within a column, and
removing columns which are not relevant to this task.
Think about how each column might be relevant to the business question you’re investigating. If you can’t think of why a column may be useful, it may not be worth including it.



Removed unnecessary variables. URL from Contnent and User ID

Looking at content, we ensured there were no blanks by using the filter in excel. There were some observations with quotation marks that caused duplicates, so we used the Replace tool in excel to remove all quotation marks. 

Looking at Reaction spreadsheet, filtered out all blanks. User ID is not relevant 

A data model shows the relationship between all the data sets

### Data modeling

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

