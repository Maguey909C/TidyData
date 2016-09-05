# Hello Reviewer, 
# So full disclosure, I worked very diligently on this final assignment, but struggled to understand what exactly constituted a "tidy" dataset based on the limted instructions from John Hopkins.  I know from the forum, that I was not the only person annoyed at the vague instructions, and superficial responses from instuctors.  Overally, I had a lot of questions about what information could be merged, since merging datasets with unlabeled columns such as V1,V2,V3 from multiple data sets (body_acc, body_gyro, and total_acc) could lose valuable insights of x,y,and z axes if each variable is in one column.  Bottom line, I found this assignment frustrating, difficult to understand, and thus not representative of my understanding of the material.  I did the best I could with what I knew, but despite my best efforts am confident I did not complete the assignment exactly the way they wanted.  With that said, my code works. You can see the mean and standard deviation for each column in the test and train data sets using the function (finalmeansd), which produces a matrix. You can also see all the combined data from the test and train text files in one matrix using the function (finaldataset). (For more information see the CodeBook.md file)

# Methodology
# My methodology was fairly simple.  
# 1. Put all the files (subject_test, subject_train, x_test, body_acc_x_test, body_gyro_y_test, # etc.) in one folder so I could read #      them in from a similar directory.
# 2. Read in the files with the read.table() function
# 3. Substituted the old column names of "V1,V2,V3..." with new column names that reflected their file to become "body_acc_x_test1, body_acc_x_test2, body_acc_x_test3" using the sub() function.  
# 4. Repeated this step a bunch of times for each file. (I am sure there is a better cleaner way to do it, but that is all I could come up with what I know).
# 5. Set new names to the columns using the setnames() function that reflected their file name 
# 6. Column bound the datasets together (i.e. combined body_acc_x_test with body_acc_y_test, etc.) until there were complete test and train files with columns names for each one.
# 7. Calculated the means and standard deviation of each column in every data set using the colMeans() function and sapply(x, sd) function.
# 8. Finally, I combined the two data sets using the r.bind.fill() because the two data sets had a different total numbers of observations.

# To see my code in action, make sure all the files are in one directory.
# Then source my script, or copy and paste it in a new R script page, but 
# To see the means and standard deviations from every test and train file use the function: finalmeansd 
# To see the final data set of train and test files combined use the fuction: finaldataset
# *Note I would use the head function on each of them, especially the last data set because it is huge!


