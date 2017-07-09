CODEBOOK - Getting and Cleaning Data Course Project

Original Data

The original data is from an experiment with a group of 30 volunteers wearing a smartphone (Samsung Galaxy S II) on the waist. The collected data is from the accelerometers from this smartphone and can be downloaded from: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The full description can be found here: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Process

The original data was merged to create one big data set in the following way:
features.txt	"Activity_ID"	"Subject_ID"
X_train.txt	y_train.txt	subject_train.txt
X_test.txt	y_test.txt	subject_train.txt
From this dataset was extract only the columns of mean and standard deviation and the "Activity_ID" and "Subject_ID" columns.

The column "Activity_ID", that has the integers that represents each type of activity, was replaced with the "Activity" columns, that has the names of each activity followin the map below:

1 WALKING
2 WALKING_UPSTAIRS
3 WALKING_DOWNSTAIRS
4 SITTING
5 STANDING
6 LAYING
The original variables names, such as tBodyAccMag-mean(), were replaced with better descriptive names, such as TimeBodyAccelerationMagnitudeMean.

An independent tidy data set was created with the mean of each activity and each subject. This new dataset was saved in the tidy_data.txt file.

Variables

There are 180 observations of 68 variables, where the Activity variable is a factor, the Subject_ID is an integer and the other variables are numbers.

Activity: The activity performed for each subject. One of WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING.
Subject_ID: The subject identifier. From 1 to 30.
