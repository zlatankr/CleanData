CODEBOOK FOR "tidy" DATASET
---------------------------------
act-name is the code for Activity Name, and the values are:
		LAYING
		SITTING
		STANDING
		WALKING
		WALKING_DOWNSTAIRS
		WALKING_UPSTAIRS

subject is the code for Participant number, and the values range from 1:30

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

tBodyAcc-XYZ
tGravityAcc-XYZ
tBodyAccJerk-XYZ
tBodyGyro-XYZ
tBodyGyroJerk-XYZ
tBodyAccMag
tGravityAccMag
tBodyAccJerkMag
tBodyGyroMag
tBodyGyroJerkMag
fBodyAcc-XYZ
fBodyAccJerk-XYZ
fBodyGyro-XYZ
fBodyAccMag
fBodyAccJerkMag
fBodyGyroMag
fBodyGyroJerkMag

The set of variables that were estimated from these signals are: 

mean(): Mean value
std(): Standard deviation

......
Here are the definitions of all the objects in the R scrips:

testX: this object is the imported X_test.txt file
testY: this object is the imported Y_test.txt file
subject_test: this object is the imported subject_test.txt file
trainX: this object is the imported X_train.txt file
trainY: this object is the imported Y_train.txt file
subject_train: this object is the imported subject_train.txt file
activity_labels: this object is the imported activity_labels.txt file
features: this object is the imported features.txt file
featurenames: this vector takes all the names of the features from the features object (for assigning variable names)
testX2: this data frame is a subset of the testX data frame to only include the columns that have mean and standard deviation
trainX2: this data frame is a subset of the trainX data frame to only include the columns that have mean and standard deviation
test: this object combines the columns of the subject_test, testY, and testX2 objects
train: this object combines the columns of the subject_train, trainY, and trainX2 objects
combined: this object combines the rows of the test and train datasets
combined2: this object merges the combined dataset witht eh activity_label dataset so that we can have the activity names
vars: this object only keeps the variable columns of the combined2 dataset
stack: this is a vertical melt of the variable columns by subject by activity
tidy: this object takes teh stack data frame and calculates the mean of the variables by subject by activity




