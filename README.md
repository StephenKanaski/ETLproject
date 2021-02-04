Project 2: ETL
By Emily Zhu, Surabhi Mukati, Stephen Kanaski, Hayden Rubin


Extract: 
•	Extracted Netflix TV shows’ IMDB ratings by web scraping. After scraping, inputted the content into a data frame. Below is a link: https://www.imdb.com/search/title/?companies=co0144901&ref_=adv_prv
•	Extracted a CSV file with a list of Netflix shows and movies from Kaggle.  https://www.kaggle.com/shivamb/netflix-shows

Transform: 
•	The data cleaning and transformation that was done on the Netflix TV shows’ IMDB ratings file consisted of:
o	Dropping shows that didn’t have any ratings. 
o	Using groupby() on the titles and using the average ratings as the rating for the shows that had multiple ratings for multiple episodes.  

•	The data cleaning and transformation that was done on the Netflix movies and shows CSV file consisted of:
o	Using loc to extract just the tv shows. 
o	Dropping columns that we weren’t interested in, but including “type”, “title”, “country”, “release year”, and “category”.  
o	Looking at the number of unique titles and dropping duplicates. 

Load: 
•	Connected our Jupyter Notebook to a local PostGres database. 
•	Exported data frames into PostGres as tables. 
•	Final tables are: Netflixratings and Netflixshows. 

