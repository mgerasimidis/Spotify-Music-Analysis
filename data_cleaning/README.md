# Data Cleaning
Here I will explain the main steps I followed in order to clean the data and use them for the exploratory data analysis.

### Data
* Dataset 1: https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2020/2020-01-21/spotify_songs.csv
* Dataset 2: https://www.kaggle.com/rodolfofigueroa/spotify-12m-songs

### Merging the dataframes
In **Dataset 1** there were around 30k tracks and in **Dataset 2** around 1.2 M tracks. Most of columns were common, but there were some problems such as:
* In **Dataset 1** there was a column called "playlist_genre" and one called "track_popularity", but these columns did not exist in **Dataset 2**.
* In **Dataset 1** there were tracks with the same "track_id" many times, since different users classified them in different genres.

Hence, I kept only the unique id's from the first dataset and then merged it to the second (the "big" one), using as key the column of the 'id', and also adding the columns "genre" and "track_popularity". In this way, instead of analyzing each dataset seperately, I decided to do my analysis once. For all the songs in the merged dataframe, I investigated the features of the tracks and the releases. For the tracks that came with "genre" and "track_popularity", I did my analysis for this features only for that tracks.
