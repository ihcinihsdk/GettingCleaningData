How does the script work?
=========================

There is only one R script which does all the work, including getting and cleaning the data. In more detail, this script does the following:
* It reads from file pairs "XXX\_train.txt" and "XXX\_test.txt" and combines corresponding values.
* It reads file "activity\_labels.txt" and transforms all activities represented in a numeric value to descriptive strings.
* From all measurement data "body\_acc\_x", "body\_gyro\_x" and "total\_acc\_x", the averages and standard deviations are computed.
* It reads from file "features.txt", and changes the names of the 561 feature vector to descriptive ones.
* It combines the following columns: activities, subjects, the averages and standard deviations of "body\_acc\_XXX", "body\_gyro\_XXX" and "total\_acc\_XXX" (XXX indicating x, y or z) and the features and we get a large data frame "all\_data".
* It groups the data frame all\_data by activity and subject, and achieves the following two new data frames: mean of all columns (except activity and subject) by activity, and mean of all columns (except activity and subject) by subject.

Note that to make the script work, it must be copied to the folder "UCI HAR Dataset".
