---
title: "Code Book_Activity Data Analysis"
output: 
  html_document:
    keep_md: true 
---

The run_analysis.R script performs the data collection and cleaning by the 5 steps described below :  

Step 1 : Loadning all the required libraries  
Step 2 : Download the zip file "UCI HAR Dataset" and extract all the files  
Step 3 : Create seperate tables with the datasets available as below:  
        1. "features" table is created using "Features.txt". It has 561 rows, 2 columns. The features available come from   
            accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ.  
        2. "activities" table is created using "activity_labels.txt".It is a dimensional table with 6 rows and 2 columns. It has   
            the names for the corresponding codes.  
        3. "subject_test" table is created using "Subject_test.txt". It has 2947 rows and 1 column. It is a test dataset of 9/30                      volunteer test subjects.  
        4. "x_test" table is created using "X_test.txt". It has 2947 rows and 561 columns. It has the recorded features of the test                 data.  
        5. "y_test" table is created using "y_test.txt". It has 2947 rows and 1 column.It has test data of activities' code labels  
        6. "subject_train" table is created using "subject_train.txt". IT has 7352 rows and 1 column. It contains train data for 21/30               volunteer train subjects.  
        7. "X_train" table is created using "X_train.txt". It has 7352 rows and 561 columns. It has the recorded features of the train               data.  
        8. "y_train" table is created using "y_train.txt". It has 7352 rows and 1 column.It has train data of activities' code labels  
Step 4 : Merges the train and test data set int a single data set. 
        "x" dataset has the merged data from x_train and x_test. It has 10299 rows and 561 columns.  
        "y" dataset has the merged data from y_train and y_test. It has 10299rows and 1 column.  
        "subject" dataset has the merged data from "subject_train" and "subject_test". It has 10299 rows and 1 column.  
        "final_merged" dataset has the data merged from the above files "x","y" and "subject".  
Step 5 : Extracts only the measurements on the mean and standard deviation for each measurement. A subset of the "final_merged" is  created called "subset",selecting only the columns subject, code and the measurements on the mean and standard deviation(std) for each   measurement.  
       
Step 6 : Gives descriptive activity names to name the activitues in the data set. 
Step 7 : Gives names to the columns with descriptive variable names. Below are the changes made:  
        1. code column in TidyData renamed into activities  
        2. All Acc in column’s name replaced by Accelerometer  
        3. All Gyro in column’s name replaced by Gyroscope  
        4. All BodyBody in column’s name replaced by Body  
        5. All Mag in column’s name replaced by Magnitude  
        6. All start with character f in column’s name replaced by Frequency  
        7. All start with character t in column’s name replaced by Time  
        8. gravity,angle is changed to Gravity and Angle  
Step 8 : From the data set above, creates a second clean data set with the average of each variable for each activity and each                subject.This data is called as "result" with 180 rows and 89 columns.  
Step 9 : Export the "result" dataset into result_activitydata_analysis.txt" with row.names=FALSE  

