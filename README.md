# Getting_Cleaning_Data_Course_Project
This repository is created as part of the Course Project for "Getting and Cleaning Data" Course offered by Johns Hopkins University on Coursera. It contains files used for cleaning data and the tidy data generated.

The file "CodeBook.md" describes the variables, the data and the transformations done to produce a tidy dataset.

The file "tidydata.txt" is the independent tidy data produced from running the "run_analysis.R" script

The file "run_analysis.R" contains the code that downloads the data from the source and performs the transformations that produce the tidy dataset.
The "run_analysis.R" script does the following:

- Sets the Working directory and creates file location
- Downloads and extracts the files from the raw data source
- Merges the training and the test sets to create one data set
- Extracts only the measurements on the mean and standard deviation for each measurement
- Uses descriptive activity names to name the activities in the data set
- Appropriately labels the data set with descriptive variable names
- Creates a second, independent tidy data set with the average of each variable for each activity and each subject
- Displays the tidy dataset
