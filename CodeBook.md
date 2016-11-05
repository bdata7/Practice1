# Code Book for the 'run_analysis.R' Script

## Description of the Raw Data Set

Data collected from accelerometers and gyroscopes on Samsung Galaxy S smartphones was gathered from the website "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip".  A complete description of the experiment can be found at "http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones".

## Data Signals, Activities, and Variables

The following signals were analyzed in this data set:

1.  tBodyAcc-XYZ
2.  tGravityAcc-XYZ
3.  tBodyAccJerk-XYZ
4.  tBodyGyro-XYZ
5.  tBodyGyroJerk-XYZ
6.  tBodyAccMag
7.  tGravityAccMag
8.  tBodyAccJerkMag
9.  tBodyGyroMag
10. tBodyGyroJerkMag
11. fBodyAcc-XYZ
12. fBodyAccJerk-XYZ
13. fBodyGyro-XYZ
14. fBodyAccMag
15. fBodyAccJerkMag
16. fBodyGyroMag
17. fBodyGyroJerkMag

The signals use abbreviated names for brevity, and a complete description of the signals is given in the 'features_info.txt' file  provided with the raw data zip file.  In general, the abbreviations are straightforward (i.e., t = time, f = frequency, BodyAcc = body acceleration, etc.).

The following activities were performed by the subjects in the experiment:

1. Walking
2. Walking Upstairs
3. Walking Downstairs
4. Sitting
5. Standing 
6. Laying

Many variables were estimated from the above signals, but only two are of interest to the data analysis performed herein:

1. mean(): Mean value
2. std(): Standard deviation

All other variables were filtered out of the raw data in the 'run_analysis.R' script.

## Study Design & Data Tidying

The raw data was taken directly from "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip".  Within the zip master file, the following files were downselected for use:

1.  UCI HAR Dataset/test/X_test.txt
2.  UCI HAR Dataset/train/X_train.txt
3.  UCI HAR Dataset/test/y_test.txt
4.  UCI HAR Dataset/train/y_train.txt
5.  UCI HAR Dataset/activity_labels.txt
6.  UCI HAR Dataset/test/subject_test.txt
7.  UCI HAR Dataset/train/subject_train.txt
8.  UCI HAR Dataset/features.txt 
     
Briefly, the test and train datasets were merged together into one.  Variables pertaining to the mean and standard deviation were extracted from the raw data.  Finally, a tidy, organized dataset was generated with the average of each variable for each activity and subject.   
 