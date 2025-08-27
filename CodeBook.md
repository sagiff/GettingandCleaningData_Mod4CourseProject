Getting and Cleaning Data - Peer-Graded Course Project for Module 4 -
CODE BOOK
================
Author: sagiff

# Project Description

The purpose of this project is to demonstrate your ability to collect,
work with, and clean a data set. The goal is to prepare tidy data that
can be used for later analysis.

Results of this assignment should include: 1) a tidy data set as
described below, 2) a link to a Github repository with the script for
performing the analysis, 3) a code book that describes the variables,
the data, and any transformations or work that were performed to clean
up the data called CodeBook.md, and 4) a README.md in the repo with the
scripts. This repo explains how all of the scripts work and how they are
connected.

## Description of the Data:

The experiments have been carried out with a group of 30 volunteers
within an age bracket of 19-48 years. Each person performed six
activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING,
STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the
waist. Using its embedded accelerometer and gyroscope, we captured
3-axial linear acceleration and 3-axial angular velocity at a constant
rate of 50Hz. The experiments have been video-recorded to label the data
manually. The obtained dataset has been randomly partitioned into two
sets, where 70% of the volunteers was selected for generating the
training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by
applying noise filters and then sampled in fixed-width sliding windows
of 2.56 sec and 50% overlap (128 readings/window). The sensor
acceleration signal, which has gravitational and body motion components,
was separated using a Butterworth low-pass filter into body acceleration
and gravity. The gravitational force is assumed to have only low
frequency components, therefore a filter with 0.3 Hz cutoff frequency
was used. From each window, a vector of features was obtained by
calculating variables from the time and frequency domain. See
‘features_info.txt’ for more details.

## Files Used:

The files used for this project included the following, with
descriptions:

- ‘features.txt’: List of all features/variables of the activity data.

- ‘X_train.txt’: Training data set.

- ‘y_train.txt’: Training activity labels.

- ‘X_test.txt’: Test data set.

- ‘y_test.txt’: Test activity labels.

- ‘subject_train.txt’: Each row identifies the subject who performed the
  activity for each window sample. Its range is from 1 to 30.

## Activity Label Descriptions:

The activity labels included in ‘y_train.txt’ and ‘X_train.txt’
correspond to the 6 activities performed as follows:

- 1 = WALKING
- 2 = WALKING_UPSTAIRS
- 3 = WALKING_DOWNSTAIRS
- 4 = SITTING
- 5 = STANDING
- 6 = LAYING

## Feature Selection - Original Data Set:

The features selected for this database come from the accelerometer and
gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain
signals (prefix ‘t’ to denote time) were captured at a constant rate of
50 Hz. Then they were filtered using a median filter and a 3rd order low
pass Butterworth filter with a corner frequency of 20 Hz to remove
noise. Similarly, the acceleration signal was then separated into body
and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ)
using another low pass Butterworth filter with a corner frequency of 0.3
Hz.

Subsequently, the body linear acceleration and angular velocity were
derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and
tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional
signals were calculated using the Euclidean norm (tBodyAccMag,
tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag).

Finally a Fast Fourier Transform (FFT) was applied to some of these
signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ,
fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the ‘f’ to
indicate frequency domain signals).

These signals were used to estimate variables of the feature vector for
each pattern:  
‘-XYZ’ is used to denote 3-axial signals in the X, Y and Z directions.

- tBodyAcc-XYZ
- tGravityAcc-XYZ
- tBodyAccJerk-XYZ
- tBodyGyro-XYZ
- tBodyGyroJerk-XYZ
- tBodyAccMag
- tGravityAccMag
- tBodyAccJerkMag
- tBodyGyroMag
- tBodyGyroJerkMag
- fBodyAcc-XYZ
- fBodyAccJerk-XYZ
- fBodyGyro-XYZ
- fBodyAccMag
- fBodyAccJerkMag
- fBodyGyroMag
- fBodyGyroJerkMag

Additional vectors obtained by averaging the signals in a signal window
sample. These are used on the angle() variable:

- gravityMean
- tBodyAccMean
- tBodyAccJerkMean
- tBodyGyroMean
- tBodyGyroJerkMean

The complete list of variables of each feature vector is available in
‘features.txt’

The relevant set of variables that were estimated from these signals
are: - mean(): Mean value - std(): Standard deviation

All other calculated variables that were not relevant to this project
were removed from the final data set.

Units for acceleration measurements are m/s^2. Units for angular
velocity are rad/s-1

## Feature Selection - Final Data Set (merged_data):

- subjectid
- activitylabel
- tbodyacc.mean.x
- tbodyacc.mean.y
- tbodyacc.mean.z
- tgravityacc.mean.x
- tgravityacc.mean.y
- tgravityacc.mean.z
- tbodyaccjerk.mean.x
- tbodyaccjerk.mean.y
- tbodyaccjerk.mean.z
- tbodygyro.mean.x
- tbodygyro.mean.y
- tbodygyro.mean.z
- tbodygyrojerk.mean.x
- tbodygyrojerk.mean.y
- tbodygyrojerk.mean.z
- tbodyaccmag.mean
- tgravityaccmag.mean
- tbodyaccjerkmag.mean
- tbodygyromag.mean
- tbodygyrojerkmag.mean
- fbodyacc.mean.x
- fbodyacc.mean.y
- fbodyacc.mean.z
- fbodyacc.meanfreq.x
- fbodyacc.meanfreq.y
- fbodyacc.meanfreq.z
- fbodyaccjerk.mean.x
- fbodyaccjerk.mean.y
- fbodyaccjerk.mean.z
- fbodyaccjerk.meanfreq.x
- fbodyaccjerk.meanfreq.y
- fbodyaccjerk.meanfreq.z
- fbodygyro.mean.x
- fbodygyro.mean.y
- fbodygyro.mean.z
- fbodygyro.meanfreq.x
- fbodygyro.meanfreq.y
- fbodygyro.meanfreq.z
- fbodyaccmag.mean
- fbodyaccmag.meanfreq
- fbodybodyaccjerkmag.mean
- fbodybodyaccjerkmag.meanfreq
- fbodybodygyromag.mean
- fbodybodygyromag.meanfreq
- fbodybodygyrojerkmag.mean
- fbodybodygyrojerkmag.meanfreq
- angletbodyaccmean.gravity
- angletbodyaccjerkmean.gravitymean
- angletbodygyromean.gravitymean
- angletbodygyrojerkmean.gravitymean
- anglex.gravitymean
- angley.gravitymean
- anglez.gravitymean
- tbodyacc.std.x
- tbodyacc.std.y
- tbodyacc.std.z
- tgravityacc.std.x
- tgravityacc.std.y
- tgravityacc.std.z
- tbodyaccjerk.std.x
- tbodyaccjerk.std.y
- tbodyaccjerk.std.z
- tbodygyro.std.x
- tbodygyro.std.y
- tbodygyro.std.z
- tbodygyrojerk.std.x
- tbodygyrojerk.std.y
- tbodygyrojerk.std.z
- tbodyaccmag.std
- tgravityaccmag.std
- tbodyaccjerkmag.std
- tbodygyromag.std
- tbodygyrojerkmag.std
- fbodyacc.std.x
- fbodyacc.std.y
- fbodyacc.std.z
- fbodyaccjerk.std.x
- fbodyaccjerk.std.y
- fbodyaccjerk.std.z
- fbodygyro.std.x
- fbodygyro.std.y
- fbodygyro.std.z
- fbodyaccmag.std
- fbodybodyaccjerkmag.std
- fbodybodygyromag.std
- fbodybodygyrojerkmag.std

## Feature Selection - Final Data Set (summary_data):

- subjectid
- activitylabel
- avg.tbodyacc.mean.x
- avg.tbodyacc.mean.y
- avg.tbodyacc.mean.z
- avg.tgravityacc.mean.x
- avg.tgravityacc.mean.y
- avg.tgravityacc.mean.z
- avg.tbodyaccjerk.mean.x
- avg.tbodyaccjerk.mean.y
- avg.tbodyaccjerk.mean.z
- avg.tbodygyro.mean.x
- avg.tbodygyro.mean.y
- avg.tbodygyro.mean.z
- avg.tbodygyrojerk.mean.x
- avg.tbodygyrojerk.mean.y
- avg.tbodygyrojerk.mean.z
- avg.tbodyaccmag.mean
- avg.tgravityaccmag.mean
- avg.tbodyaccjerkmag.mean
- avg.tbodygyromag.mean
- avg.tbodygyrojerkmag.mean
- avg.fbodyacc.mean.x
- avg.fbodyacc.mean.y
- avg.fbodyacc.mean.z
- avg.fbodyacc.meanfreq.x
- avg.fbodyacc.meanfreq.y
- avg.fbodyacc.meanfreq.z
- avg.fbodyaccjerk.mean.x
- avg.fbodyaccjerk.mean.y
- avg.fbodyaccjerk.mean.z
- avg.fbodyaccjerk.meanfreq.x
- avg.fbodyaccjerk.meanfreq.y
- avg.fbodyaccjerk.meanfreq.z
- avg.fbodygyro.mean.x
- avg.fbodygyro.mean.y
- avg.fbodygyro.mean.z
- avg.fbodygyro.meanfreq.x
- avg.fbodygyro.meanfreq.y
- avg.fbodygyro.meanfreq.z
- avg.fbodyaccmag.mean
- avg.fbodyaccmag.meanfreq
- avg.fbodybodyaccjerkmag.mean
- avg.fbodybodyaccjerkmag.meanfreq
- avg.fbodybodygyromag.mean
- avg.fbodybodygyromag.meanfreq
- avg.fbodybodygyrojerkmag.mean
- avg.fbodybodygyrojerkmag.meanfreq
- avg.angletbodyaccmean.gravity
- avg.angletbodyaccjerkmean.gravitymean
- avg.angletbodygyromean.gravitymean
- avg.angletbodygyrojerkmean.gravitymean
- avg.anglex.gravitymean
- avg.angley.gravitymean
- avg.anglez.gravitymean
- avg.tbodyacc.std.x
- avg.tbodyacc.std.y
- avg.tbodyacc.std.z
- avg.tgravityacc.std.x
- avg.tgravityacc.std.y
- avg.tgravityacc.std.z
- avg.tbodyaccjerk.std.x
- avg.tbodyaccjerk.std.y
- avg.tbodyaccjerk.std.z
- avg.tbodygyro.std.x
- avg.tbodygyro.std.y
- avg.tbodygyro.std.z
- avg.tbodygyrojerk.std.x
- avg.tbodygyrojerk.std.y
- avg.tbodygyrojerk.std.z
- avg.tbodyaccmag.std
- avg.tgravityaccmag.std
- avg.tbodyaccjerkmag.std
- avg.tbodygyromag.std
- avg.tbodygyrojerkmag.std
- avg.fbodyacc.std.x
- avg.fbodyacc.std.y
- avg.fbodyacc.std.z
- avg.fbodyaccjerk.std.x
- avg.fbodyaccjerk.std.y
- avg.fbodyaccjerk.std.z
- avg.fbodygyro.std.x
- avg.fbodygyro.std.y
- avg.fbodygyro.std.z
- avg.fbodyaccmag.std
- avg.fbodybodyaccjerkmag.std
- avg.fbodybodygyromag.std
- avg.fbodybodygyrojerkmag.std

## Description of Data Transformations:

1.  The file containing the variable names (features.txt) was read into
    R as a data frame and the rows containing the variables were
    transposed to columns. Additional white spaces were removed.
2.  The variable names were cleaned up: changed all letters to
    lowercase, removed parentheses, changed “-” and “,” to “.”.
3.  The other files (subject_test.txt, X_test.txt, y_test.txt,
    subject_train.txt, X_train.txt, y_train.txt) were read into R as
    data frames. Column names were added and additional white spaces
    were removed. The column names for X_test and X_train were added
    using the variable names from features.
4.  The activity labels in y_test and y_train were changed from numbers
    to characters (1=walking, 2=walkingupstairs, 3=walkingdownstairs,
    4=sitting, 5=standing, 6=laying).
5.  The files for test (subject_test containing subject ids, y_test
    containing activity labels, and X_test containing activity data)
    were combined into one data frame.
6.  The files for train (subject_train containing subject ids, y_train
    containing activity labels, and X_train containing activity data)
    were combined into one data frame.
7.  The files for test and train were combined into one data frame and
    sorted by subject id called merged_data.
8.  The merged_data was filtered to keep only measurements for mean and
    standard deviation.
9.  A second independent data frame called summary_data was created
    which contained the average for each variable for each activity and
    each subject.
