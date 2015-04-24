## Code Book

This code book will describe the data used in this project, as well as the processing required to create the resulting tidy data set.

### Overview

- 30 volunteers performed 6 different activities while wearing a smartphone
- Smartphones captured various data about their movements.

### Files Used

- `features.txt`: Names of the 561 features.
- `activity_labels.txt`: Names and IDs for each of the 6 activities.

- `X_train.txt`: 7352 observations of the 561 features, for 21 of the 30 volunteers.
- `subject_train.txt`: A vector of 7352 integers, denoting the ID of the volunteer related to each of the observations in `X_train.txt`.
- `y_train.txt`: A vector of 7352 integers, denoting the ID of the activity related to each of the observations in `X_train.txt`.

- `X_test.txt`: 2947 observations of the 561 features, for 9 of the 30 volunteers.
- `subject_test.txt`: A vector of 2947 integers, denoting the ID of the volunteer related to each of the observations in `X_test.txt`.
- `y_test.txt`: A vector of 2947 integers, denoting the ID of the activity related to each of the observations in `X_test.txt`.

### Analysis Path

1. The above data files were read into data frames, column headers were added, and training & test sets were combined into a single data set.
2. Feature columns that did not contain the exact string "mean()" or "std()" were removed; leaving 66 feature columns, subjectID, and activity columns.
3. Activity column was converted from a integer to a factor, using labels describing the activities.
4. A tidy data set was created containing the mean of each feature for each subject and each activity. Ouput is a CSV file.
5. Subject #1 has 6 rows in the tidy data set (one row for each activity)
6. Each row contains the mean value for each of the 66 features for that subject/activity combination.
7. For the total 30 subjects, there are a 180 rows.

