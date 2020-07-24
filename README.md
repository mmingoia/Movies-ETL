# Movies-ETL

UTDA Module 8

## Challenge Work

For this challenge the code that was created for the lesson was refactored to perform the same task of performing ETL on movie data, but exploratory data analysis was removed and the python script was modified to be used as a function so similar data could be used in the future with minimal changes to the code.

There are some assumptions that must be made in order for this function to work.  The first assumption is that the format of the data is kept the same: Wikipedia in JSON, Kaggle metadata and rating data in csv as well as being stored in the "data" directory.  Different files could be used, but the names would have to be updated in the script.  A second assumption would be that the column names from the data have to match the existing data structure.  If different data is included the code would have to be adjusted.  Third, because regular expressions were used to standardize the box office revenue, budget and release date, if the data has a significant amount on new formats introduced the current regular expressions may need to be updated.  Also, when the wiki and kaggle data was merged there were 7 columns that matched.  In 4 instances the wiki data was dropped, in the other 3 the wiki data was used to fill in gaps in the kaggle data.  With a different dataset this may need to be updated depending on the quality of each dataset.  Fourth the script currently drops Adult Movies and "movies" with episodes that are likely TV shows from the data.  Finally, in order for this function to work, a Postres database with the name "movie_data" must be on the local computer.  The name and location of the database could be adjusted but the function would have to be updated.

Throughout the function I have added several "try-except" blocks that will print an message to identify when errors occur.  If errors occur these should help find the code with issues to correct the code based when being used on new data.
