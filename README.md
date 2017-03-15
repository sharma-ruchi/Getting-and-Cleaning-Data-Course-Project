This project will read the training and test data measurements from UCI.The included scripts will read, merge, process, and analyse data in order to tidy it up for analysis.

Running the Script
Inside the working directory, source("run_analysis.R").
The script is assuming the unzipped directory of the data is already there. 
If not, then run download_uci_data().
Otherwise, just type run_analysis()
This function will return the tidy data table and create an equivalent output file : activitydata_tidy.txt.

Important variables
train_df - Merged training data frame from subject_data, Xdata, and ydata of training directory.
test_df - Merged test data frame from subject_data, Xdata, and ydata of test directory.
alldata_df - Merged train_df and test_df with labels for the columns.
activity_cleandf - the "clean" extracted data from 
alldata_df with only "mean" and "std" vectors.  Also has translated "activity_name" vector to provide a name for activity number.
activity_tidydf - final output of tidy dataset, with rows grouped by subject and activity with mean of each feature vector.

Dependency
dplyr - used to aggregate and run mean calculation.

Files:
README.md
This markdown file.

run_analysis.R
This project will read and download data into the working directory and perform the following steps to clean the data.
Merges the training and the test sets to create one data set.
Extracts only the measurements on the mean and standard deviation for each measurement.
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive variable names.
From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

Data:
Data file is downloaded from link provided by Coursera Instructor (see below):
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Further information on this data set can be found at:http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

In general, this data is taken from 30 volunteers using body trackers to determine what activities they were doing. 
In order to build the tidy data tables in R, the following files were used. 

"UCI HAR Dataset/train/subject_train.txt" - Table describing which user generated the measurement sample in the row.
"UCI HAR Dataset/train/X_train.txt" - Data of the measurement samples per feature used and described by features_info.txt
"UCI HAR Dataset/train/y_train.txt" - Activity code of the action represented by the measurement sample.
"UCI HAR Dataset/test/subject_test.txt" - Table describing which user generated the measurement sample in the row.
"UCI HAR Dataset/test/X_test.txt" - Data of the measurement samples per feature used and described by features_info.txt
"UCI HAR Dataset/test/y_test.txt" - Activity code of the action represented by the measurement sample.
"UCI HAR Dataset/activity_labels.txt" - activity labels for each numeric code.
"UCI HAR Dataset/features.txt" - Name of each column/feature of X_test.txt.
"UCI HAR Dataset/features_info.txt" - Description of the features of X_Test.txt.
