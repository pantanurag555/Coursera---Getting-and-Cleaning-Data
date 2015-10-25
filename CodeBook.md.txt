##Working of the run_analysis.R Script##

The script performs the 5 steps described in the course project:-
<ul>
<li>Similar data is merged using rbind. This is the data having similar entities and same number of columns.
<li>The columns with the mean and standard deviation are taken then from the dataset. The columns are then named using the names from features.txt.
<li>Activity names are substituted in the dataset from activity_labels.txt.
<li>Remaining columns are given their proper names.
<li>A new tidy dataset is created with the average of each variable for each activity and each subject called average_data.txt.
</ul>

##Variables##

<ul>
<li>x_train, y_train, x_test, y_test, subject_train and subject_test store the data from the files.
<li>x_data, y_data and subject_data merge the similar datasets together.
<li>features contains the column names for the x_data dataset, which are applied to the mean_and_std_features, a numeric vector used to find the required columns.
<li>activities contains the name of the various activities and is used in naming them in the y_data dataset.
<li>all_data merges x_data, y_data and subject_data into one dataset.
<li>avg_data contains the averages which are then stored in a .txt file. ddply() from the plyr package is used to apply colMeans() to the dataset.
</ul>