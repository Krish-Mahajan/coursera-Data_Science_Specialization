Getting and Cleaning Data Course Project
========================================

###Guidelines  
The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The
goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a
series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as
described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a
code book that describes the variables, the data, and any transformations or work that you performed to
clean up the data called CodeBook.md. You should also include a README.md in the repo with your
scripts. This repo explains how all of the scripts work and how they are connected.  

One of the most exciting areas in all of data science right now is wearable computing see
for example
this article (http://www.insideactivitytracking.com/datascienceactivitytrackingandthebattlefortheworldstopsportsbrand/).
Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most
advanced algorithms to attract new users. The data linked to from the course website represent data
collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available
at the site where the data was obtained:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
(http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)
Here are the data for the project:  

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
(https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)  

You should create one R script called run_analysis.R that does the following.
1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names.
5. From the data set in step 4, creates a second, independent tidy data set with the average of each
variable for each activity and each subject. 

### Project Report
This file describes how run_analysis.R script works.
* First, unzip the data from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip and rename the folder with "data".
* Make sure the folder "data" and the run_analysis.R script are both in the current working directory.
* Second, use source("run_analysis.R") command in RStudio. 
* Third, you will find two output files are generated in the current working directory:
  - merged_data.txt (7.9 Mb): it contains a data frame called cleanedData with 10299*68 dimension.
  - data_with_means.txt (220 Kb): it contains a data frame called result with 180*68 dimension.
* Finally, use data <- read.table("data_with_means.txt") command in RStudio to read the file. Since we are required to get the average of each variable for each activity and each subject, and there are 6 activities in total and 30 subjects in total, we have 180 rows with all combinations for each of the 66 features. 
