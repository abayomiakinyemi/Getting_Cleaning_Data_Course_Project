# **Code Book**

This code book is prepared as part of the Course Project for "Getting and Cleaning Data" - a course in the Data Science Specialization by Johns Hopkins University on Coursera

## Introduction

This code book describes the variables, the data, and transformations performed to clean up data generated from experiments carried out with a group of 30 volunteers within an age bracket of 19-48 years where each person performed six activities (WALKING, WALKING UPSTAIRS, WALKING DOWNSTAIRS, SITTING, STANDING, LAYING) while wearing a smartphone (Samsung Galaxy S II) on the waist. 

The samrtphone using its embedded accelerometer and gyroscope was used to capture the raw data (3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz) generated in the experiments. The obtained dataset is randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

A full description is available at the site where the data was obtained:

<http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones>

## Raw Data 
###Source

The raw data was downloaded from the UCI Machine Learning Repository using the link below:

<https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip>

### Description

The dataset includes the following files:

+ 'README.txt': Gives the description of the files and data available in the dataset
+ 'features_info.txt': Shows variables information used on the _features_ variable
+ 'features.txt': Shows a list of all features.
+ 'activity_labels.txt': Links the class labels with their activity name.
+ 'train/X_train.txt': Training set.
+ 'train/y_train.txt': Training labels.
+ 'test/X_test.txt': Test set.
+ 'test/y_test.txt': Test labels.

The following files are available for the train and test data.

+ 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.

+ 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis.

+ 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration.

+ 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second.


## Data Transformation

Cleaning the raw data was done using the R script called run_analysis.R in this repository

The script does the following:

- Sets the Working directory and creates file location using:
```{r}
setwd()
if(!file.exists()){
        dir.create()
```
- Downloads and extracts the files from the raw data source using:
```{r}
download.file()
unzip()
list.files()
```
- Merges the training and the test sets to create one data set using:
```{r}
read.table(file.path())
rbind()
names()
cbind()
```
- Extracts only the measurements on the mean and standard deviation for each measurement using:
```{r}
grep()
subset()
```
- Uses descriptive activity names to name the activities in the data set using:
```{r}
read.table(file.path())
factor()
```
- Appropriately labels the data set with descriptive variable names using:
```{r}
names()
gsub()
```
- Creates a second, independent tidy data set with the average of each variable for each activity and each subject using:
```{r}
library(plyr)
aggregate()
order()
write.table()
```

The scripts also displays the tidy dataset.


