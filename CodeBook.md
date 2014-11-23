CodeBook
=========

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




