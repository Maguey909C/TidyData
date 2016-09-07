#Getting and Cleaning Data 

## Methodology
### 1. Read in the files with the read.table() function
### 2. Merge the training and test datasets.
### 3. Extract the means and standard deviation of each column in every data set using the colMeans() function and sapply(x, sd) function.
### 4. Appropriately label the columns of each data set and other relevant information
### 5. Column bind the datasets to create an separate independent tidy data set.

## Prerequisite 
### 1. Data from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip, is downloaded and unzipped into a "localPath"
### 2. Make sure the plyr library is installed

## Steps
### 1. Read the activity_labels (will be later used to replace the Factor, to satisfy REQUIREMENT #4) 
### 2. Read the feature names from features.txt. Remove "()" from the names, and make the feature names "clean" (will be used for column names, to satisfy REQUIREMENT #4) 
### 3. Read the X_train and X_test files, and extract the "standard deviation" and "mean" data for the various parameters only. 
### 4. Read the y_train and y_test; and subject_test and subject_train data. 
### 5. Add subject and activity columns to the X_train and X_test dataframes. 
### 6. rbind the test and train datasets 
### 7. Use the ddply to split the merged dataset, based on Subject and Activity; and apply the mean function 
### 8. Write to csv or txt file
