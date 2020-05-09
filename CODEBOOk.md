The run_analysis.R script performs the data preparation and then followed by the 5 steps required as described in the course project’s definition.

# Download the dataset
Dataset downloaded and extracted under the folder called UCI HAR Dataset

# Assign each data to variables
featureNames <- features.txt : 561 rows, 2 columns
The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ.

activityLabels <- activity_labels.txt : 6 rows, 2 columns
> List of activities performed when the corresponding measurements were taken and its codes (labels)

subjectTest <- test/subject_test.txt : 2947 rows, 1 column
> contains test data of 9/30 volunteer test subjects being observed

featuresTest <- test/X_test.txt : 2947 rows, 561 columns
> contains recorded features test data

activityTest <- test/y_test.txt : 2947 rows, 1 columns
> contains test data of activities’code labels

subjectTrain <- test/subject_train.txt : 7352 rows, 1 column
> contains train data of 21/30 volunteer subjects being observed

featuresTrain <- test/X_train.txt : 7352 rows, 561 columns
> contains recorded features train data

activityTrain <- test/y_train.txt : 7352 rows, 1 columns
> contains train data of activities’code labels

# Step 1: Merges the training and the test sets to create one data set

1.1 features (10299 rows, 561 columns) is created by merging featuresTrain and featuresTest using rbind() function

1.2 activity (10299 rows, 1 column) is created by merging activityTrain and activityTest using rbind() function

1.3 Subject (10299 rows, 1 column) is created by merging subjectTrain and subjectTest using rbind() function

1.4 completeData (10299 rows, 563 column) is created by merging Subject, features and activity using cbind() function

# Step 2 Extracts only the measurements on the mean and standard deviation for each measurement
extractedData (10299 rows, 88 columns) is created by subsetting completeData, 
selecting only columns: subject, code and the measurements on the mean and standard deviation (std) for each measurement

# Step 3 Uses descriptive activity names to name the activities in the data set
Entire numbers in code column of the extractedData replaced with corresponding activity taken from second column of the activities variable

# Step 4 Appropriately labels the data set with descriptive variable names
code column in extractedData renamed into activities

4.1 All Acc in column’s name replaced by Accelerometer

4.2 All Gyro in column’s name replaced by Gyroscope

4.3 All BodyBody in column’s name replaced by Body

4.4 All Mag in column’s name replaced by Magnitude

4.5 All start with character f in column’s name replaced by Frequency

4.6 All start with character t in column’s name replaced by Time

# Step 5 From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject
5.1 TidyData (180 rows, 88 columns) is created by sumarizing extractedData taking the means of each variable for each activity and each subject, after groupped by subject and activity.

5.2 Export TidyData into Tidy.txt file.
