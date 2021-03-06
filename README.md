# Movies-ETL

The course material provided guidance on how to extract and transform data and helped us clean a number of columns in the merged data from Wikipedia and Kaggle.  I extensively cleaned the remaining columns, relying heavily on the use of regex expressions, and got it ready to load to Postgres, along with the MovieLens movie rating data.  I loaded the data in postgres and checked the data to make sure that the cleaned data and movie ratings had transferred properly.

Once that was done, I automated the ETL pipeline load process in Jupyter,  setting up a function to delete the table data in the PostGres "movie_data" database prior to loading the next, fresh version of data.  Part of that process was (through automation) changing the column names in the ratings.csv to make it easier to work with the data when I bring the data back from Postgres.

The next step was to access the table data from PostGres using a try-except block to check that I was able to connect with PostGres using psycopg2 and then alerting me to issues (if encountered) connecting and/or errors arising.

Once the data was back into Jupyter, I set up a SQL query to match the ratings data to the cleaned set of movies and calculating a count of times a movie was rated as well as the average rating per movie.  I then added the summary rating information to the movie list through a dataframe merge.  I exported the merged dataframe to a csv file called "movies_rated.csv", which you'll find in my Github repository.  The code from my Jupyter notebook has been saved to the challenge.py file, per the instructions in the challenge.  It may also be found in the repository (along with the Jupyter notebook, titled challenge8.ipynb).



P.S. - added csv files (movies_metadata.csv and ratings.csv) via LFS upload at 5:15 pm PST on Sunday, March 8.