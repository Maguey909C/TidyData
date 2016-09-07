## CodeBook
The following information will the meaning behind specific variables as well as the steps I took to produce the tidy data set.

## Prerequisites
#### 1. Download the raw data sets from the following url: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
#### 2. Unzip the file and place relevant files in your working directory
#### 3. Set your working directory 
#### 4. Make sure the following packages are installed and loaded: dplyr, data.table

## Methodology
#### 1. Read in the relevant files into R from the zip files, specifically: X_train, y_train, X_test, y_test, subject_train, subject_test, features.txt 
#### 2. Column bind the relevant test and train data files
#### 3. Row bind the two data sets to have complete test and train files in one matrix
#### 4. Extract the mean and standard deviation columns from the large data set using grep
#### 5. Substitute activity names using the factor function 
#### 6. Substitute the ambigious remaining column headers using the gsub function
#### 7. Create an independent dataset based on this newly cleaned up information
#### 8. Write this new dataset to a txt or csv file

##Variables 
#### 1. X_train, y_train, X_test, y_test, subject_train, and subject_test contain data from the train and test folders
#### 2. features contains the labels for the activites 1-6
#### 3. test_data represents the column bind for the relevant test files; train_data represents the column bind for the relevant train files; and full_data represents the row bind of test_data and train_data
#### 4. features_index represents the command to extract the characters mean and standard deviation from specified columns
#### 5. final data represents a data set of only mean and standard deviation values extracted from full_data set
#### 6. tidy_data represents the newly written clean data set with appropriately labeled columns highlighting the mean and standard deviation of the relevant test and train files


