Getting and Cleaning Data Course Project

The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set.

Review criteria
1. The submitted data set is tidy.
2. The Github repo contains the required scripts.
3. GitHub contains a code book that modifies and updates the available codebooks with the data to indicate all the variables and summaries calculated, along with units, and any other relevant information.
4. The README that explains the analysis files is clear and understandable.
5. The work submitted for this project is the work of the student who submitted it.

Objectives

run_analysis.R performs the following:
1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names.
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.


run_analysis.R overview

To compelte the above objectives, execute "run_analysis.R". The data will download directly from the source, extract it and format the data. "Run-analysis.R" perfoms the follwing functions:

1. It will download the UCI HAR Dataset and put the zip file in your working directory. After it is downloaded, it unzips the file. 
2. Using Rbind, it loads the train adn test data sets and appends them into one data frame.
3. Using grep, it extracts only the mean and standard deviation from the features data set.
4. Columns names are cleaned and applied to the "x" data frame.
5. Activites data set is loaded, converted to lower case and removes the underscore. Activities and subject column names are named for y and subj data sets. 
6. The data sets, "x", "y" and "subj" are merged. Then it is exported as a txt file in the project folder, named merged.txt.
7. The mean of the activities and subjects are created into a separate tidy data set, called average.txt. 