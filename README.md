# Databaseweek15
     1. Data Dive
Dataset Selection: Netflix Shows
Difficulties Encountered:
The Netflix Shows dataset might have inconsistencies in how data is entered (e.g., different spellings of show titles or genres), which could affect analysis.
Handling missing or incomplete data entries, especially in fields like release year or country of origin.
Interesting Observation:
One interesting thing about the Netflix Shows dataset is the diversity of genres and how they have evolved over the years. For example, you might notice a shift from traditional genres to more niche categories as Netflix's content library expanded.
        
        2. Data Fun
SQL Queries:
sql
Copy code
-- Fact 1: Count of shows by genre
SELECT genre, COUNT(*) AS num_shows
FROM netflix_shows
GROUP BY genre
ORDER BY num_shows DESC
LIMIT 5;

This query will give us the top 5 genres by the number of shows.
sql
Copy code
-- Fact 2: Average rating of shows released each year
SELECT release_year, AVG(rating) AS avg_rating
FROM netflix_shows
WHERE rating IS NOT NULL
GROUP BY release_year
ORDER BY release_year;

This query calculates the average rating of shows released each year, helping us understand trends in audience reception over time.
       
       3. Ask Away

Question 1: What are the top 5 countries with the most Netflix shows?
SQL Query:
sql
Copy code
SELECT country, COUNT(*) AS num_shows
FROM netflix_shows
WHERE country IS NOT NULL
GROUP BY country
ORDER BY num_shows DESC
LIMIT 5;

Answer: From the query, we can learn which countries have produced the most shows available on Netflix.
          
          Question 2: Which are the top 10 highest-rated Netflix shows?
SQL Query:
sql
Copy code
SELECT title, rating
FROM netflix_shows
WHERE rating IS NOT NULL
ORDER BY rating DESC
LIMIT 10;

Answer: This query will provide us with the titles and ratings of the top 10 highest-rated shows on Netflix according to the dataset.
           
           Conclusion
Through these steps, we can effectively explore and analyze the Netflix Shows dataset using SQL queries. Each query helps us uncover insights such as popular genres, average ratings over time, top-producing countries, and highest-rated shows. Visualizing these findings can further enhance understanding and presentation of the insights gained from the dataset.
