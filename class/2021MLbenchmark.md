# 2021 Machine Learning Project Benchmark

**Project Manager: Bishal** 
* His EDA solution: [template](EDA-Template.ipynb)

# Objectives

The Common Core of Data (CCD) is the Department of Education's primary database on public elementary and secondary education in the United States. CCD is a comprehensive, annual, national database of all public elementary and secondary schools and school districts [link](https://nces.ed.gov/ccd/). There are seven categories of data. Within each category, data are organized by year. Within each year, there are four or five different data files. The overall objective of this task is to design and evaluate prediction of high poverty stricken school from the publicly available data, and to evaluate the value of Title 1 school designation. 

![Data1](Data1.png)

## Objectives and Tasks 

The overall objective of this task is to design and evaluate prediction of high poverty stricken school from the publicly available data accross the U.S., and to evaluate the value of Title 1 school designation. 

# Task 1. Data Integration and Exploratory Data Analysis 

You will create an integrated panel dataset that identify each public ementary and secondary schools/school districts/states. In this light your task will be to: 

1. Download data: Working with the raw data files can be tedious and time-consuming. Some data file sizes, especially for student membership data, may be over 1GB. You may find it easier to get the data you need from the Table Generator. The table generator provides access to all the years, levels and components of CCD data in an easy-to-use process you control. 
  * Focus on the State or Texas or the South Region for feasibility study before Nov 18th midterm check point
  * Focus on the subset of surveys fore the first pass, you do not need to use all 7 - use min 3 for a feasible study before Nov 1th midterm.
  * Revisit after the first pass through the pipeline (Task 1 -task 4) is complete

![Format1](Format1.png)

2. Merge data by school/school district, year, and save as .csv or .h5:  These data files need to be merged by their school IDs (NCESSCH), school district IDs (LEAID).  There are other IDs that will be helpful when merging files.
* Document data file size and entries.  
* For more advanced users, consider MongoDB or MYSQL for ingestion and manipulation

3. Exploratory data analysis of the data wrt race, poverty level, and time: This dataset will have a lot of information about the enrollment size, share of students on free and reduced lunch status (poverty proxy), and special education students, and some information about teachers. 
* Correlation matrix, data visualization, refer to Seaborn tutorials in practice folder or EDA-Template tutorial. 

*Task 1 Deliverables: python notebook and data files for all subtasks*

# Task 2. Data Separation and Ground Truth Analysis 

Lets consider all avaialbe data from 1986 to 2021 (34 school years) as 5 datasets in the following table: 

|Name | Ground Truth Labeling | Feature Selection | Modeling | Model Selection | Test |
|-----| --------------------- | ----------------- | -----------------| --------------- | ----------------| 
|Span | 1986-1991 (5)         | 1991 - 1996 (5)   | 1996 - 2014 (20) | 2014 - 2019 (5) | 2019 - 2021 (2) |

1. Title 1 designation and high percentage of free/reduced lunches should correlate.  Analyze free and reduced lunch status (poverty proxy)  and its correlation to Title 1 schools in 1986-1991 data and decide for the best  threshold for % free and reduced lunches label to create 2 new ground truth labels:  2 - SP - Strict Poverty (high threshold); 1 - HP - High Poverty (more inclusive), and 0 - no poverty.  Justify your decision.  
2. Create new labels of the data 1991 - 2021 based on the findings. 
   * Remove reduced lunch % as feature and add 1 column for poverty where 2 stands for strict 1 stands for high and 0 stands for no poverty 
   * NOTE: if easier, create 2 columns one for strict, one for high poverty. Note that strict poverty is a subset of high poverty

*Task 2 Deliverables: data files, python notebook explaining the process*

# Task 3, Option 1: 

Design a high poverty prediction model as following: 
1. Select features from Feature Selection (1991-1996) set using ground truth labels from Task 2. Use what you have learned in the class on feature selection. 
  * Pick large set of features that seem to somewhat matter for all 3 labels. 
  * Note that when evaluating for Strict poverty you are interpreting column for powerty as 2 different labels:
     * high_category = x>0?1:0, and for strict = x>1?1:0

2. Use Modeling Set for cross-validation of multiple models (1996-2014) for each of the 3 labels (Title 1, SP, HP). 
   * This is where you tune your models (.fit) and cross-validate the parameters using 5-fold  

3. Model selection using Model Selection (2014-2019) set, separately for all 3 labels: Title 1, SP, HP. 

*Task 3 Deliverables: model files, python notebook explaining the process, new .csv files.*

# Task 3, Option 2: 

Design a high poverty prediction model using temporal modeling:
* Use Modeling (1996-2014) to train multiple temporal models for all 3 label prediction 
  * Hint: check for Title 1 change or HP. SP label change over years before deciding on the segments 
* Use Model selection using Model Selection (2014-2019) set, separately for all 3 labels: Title 1, SP, HP. 

*Task 3 Deliverables: model files, python notebook explaining the process*

# Task 4 

Discuss your findings using python notebook exploratory data and model analysis
  * Visualize model outputs (HW #6) on Selection and Test data
  * Compare different model scores int he table on Selection and Test data. 
  * Illustrate and compare the results using graphs 
  * Analyze results wrt region and student race. 
  * What is a better label (Title 1 or reduced lunch threshold) for poverty stricken schools? Why? 
  * what other insights did you gain from analyzing the data. 
  
*Task 4 Deliverables: python notebook and saved figures, tables for final presentation*
 
 
