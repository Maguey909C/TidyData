#Hello again,
#The following explanation will help understand what functions I created, what they demonstate, and how to interpret my data set from my R script.
# 1. The function finaltest produces a matrix of every Test file
# 2. The function finaltrain produces a matrix of every Train file 
# 3. The function Meanfinaltest produces a matrix of all the means from all the Test files 
# 4. The function Meanfinaltrain produces a matrix of all the means from all the Train files 
# 5. The function SDfinaltest produces a matrix of standard deviations from each column in every Test file 
# 6. The function SDfinaltrain produces a matrix of  standard deviations from each column in every Train file  
# 7. The function finalmeansd produces a matrix of all the means and standard deviations from all the Train and Test files
# 8. The function finaldataset produces a matrix of every Test and Train file 

# Note, finaldataset is enormous and contains a number of NA's because the finaltest dataset and the finaltrain data set contained a different number of observations.  Like I said, I am confident how I combined these two datasets was not exactly how I should have done it, but this was what I understood from the assignment.  
# Also, I could not calculate the final mean and standard deviation from the finaldataset because of the number of NAs, and the overwhelming feeling of wanting to be done with this assignment.  
 
# When looking at a particular matrix you will see that I incorporated the name of the file in each column.  For example, a column name of body_acc_x_test1 means that it is the body_acc_x_test file and the (1) means that it was the first column, (i.e. V1), in the original file when I read it into R with read.table function.  
# Like I said before, after reading in a file into R, I could not tell if I was suppposed to keep the many columns (V1:V128) for each file (body_acc_x_test, body_acc_x_train, etc.)  So in the end, I chose to error on the side of more information for each column just in case we would need to refer back to a specific column from a specific file from the test and train data sets.  More information for each columnname allows the user to recall a observation, row, or column from every dataset from any Test or Train file.
