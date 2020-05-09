# Background of Peer-graded Assignment: Getting and Cleaning Data Course Project
This reposotory is a work of Nantana as a submission for Getting and Cleaning Data Course Project. It includes the instruction on how to run analysis in R. 
# Dataset
Human Activity Recognition Using Smartphones Data Set obtained from UCI Machine Learning Repository. 
The data represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Here are the data for the project:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
# Files submitted 
1. The tidy data set created in step 5 of the instructions named "Tidy.txt"
2. R script called "run_analysis.R"
3. "Codebook.md" describing the variables
4. "README.md" describing how the scripts work
# About the R script
I have created one R script called "run_analysis.R" that does 5 steps of collecting, working with, and cleaning a data set as follows:
1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names.
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

The "run_analysis.R" performs five steps in accordance with a task instruction. The output of the code is the tidy data set, named "Tidy.txt" which is submitted for part 1 of this assignment. 
