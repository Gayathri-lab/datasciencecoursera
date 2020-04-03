---
title: "README"
output: 
  html_document:
    keep_md: true 
---

#Getting and Cleaning Activity Data


This is a guide to explain teh files presented for the project that analyzes the Human activity recognition dataset .

Dataset considered:
[Human Activity Recognition Using Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

Files Presented :
"Code Book.md" a code book that explains the stes followed in getting and cleaning the data.
"run_analysis.R" performs the data preparation and then followed by the 8 steps required as below:

 1. Loading libraries
 2. Reading common datasets
 3. Merges the training and the test sets to create one data set.
 4. Extracts only the measurements on the mean and standard deviation for each measurement.
 5. Uses descriptive activity names to name the activities in the data set
 6. Appropriately labels the data set with descriptive variable names.
 7. From the data set in above step , creates a second clean data set with the average of each variable for each activity and each           subject.
 8. Result.txt is the exported final data after going through all the sequences described above
