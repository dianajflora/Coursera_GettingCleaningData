## Getting and Cleaning Data Course Project

### Description
The assignment requires a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data

### Source Data
A full description of the data used in this project can be found at [The UCI Machine Learning Repository](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

[The source data for this project can be found here.](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)

### Data Set Information
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

### Attribute Information
For each record in the dataset it is provided: 
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration. 
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

### 1st Task: Merge the training and the test sets to create one data set.
A. After setting the appropriate directory, read into tables the data located in
- features.txt
- activity_labels.txt
- subject_train.txt
- x_train.txt
- y_train.txt
- subject_test.txt
- x_test.txt
- y_test.txt
B. Assign column names to the data imported above.
C. Create the final training set by merging yTrain, subjectTrain, and xTrain.
D. Read in the test data.
E. Assign column names to the test data imported above.
F. Create the final test set by merging the xTest, yTest and subjectTest data.
G. Combine training and test data to create a final data set.
H. Create a vector for the column names from the finalData, which will be used to select the desired mean() & stddev() columns.

## 2nd Task: Extract only the measurements on the mean and standard deviation for each measurement. 
A. Create a logicalVector that contains TRUE values for the ID, mean() & stddev() columns and FALSE for others.
B. Subset finalData table based on the logicalVector to keep only desired columns.

## 3rd Task: Use descriptive activity names to name the activities in the data set
A. Merge the finalData set with the acitivityType table to include descriptive activity names.
B. Update the colNames vector to include the new column names after merge.

## 4th Task: Appropriately label the data set with descriptive activity names.
A. Clean up the variable names.
B. Reassign the new descriptive column names to the finalData set.

## 5th Task: From the data set in step 4, create a second, independent tidy data set with the average of each variable for each activity and each subject. 
A. Create a new table, finalDataNoActivityType without the activityType column.
B. Summarize the finalDataNoActivityType table to include just the mean of each variable for each activity and each subject.
C. Merge the tidyData with activityType to include descriptive acitvity names.
D. Export the tidyData set.
