# Movie-Data-SQL
SQL practice project analyzing a movie dataset to extract key insights.


SELECT title, genre, box_office
FROM movies_sql_practice_dataset
ORDER BY box_office DESC
LIMIT 5;
--TOP 5 HIGHEST GROSSING MOVIES

SELECT genre, AVG(rating) AS avg_rating
FROM movies_sql_practice_dataset
GROUP BY genre
ORDER BY avg_rating ASC;
-- Movie rating averages by genre in ASC order

SELECT genre, AVG(box_office) AS avg_box_office
FROM movies_sql_practice_dataset
GROUP BY genre
ORDER BY avg_box_office ASC
LIMIT 1;
-- Movie Genre with the lowest grossing average

SELECT year, COUNT(*) AS number_of_movies
FROM movies_sql_practice_dataset
group by year
order by number_of_movies DESC;
--Number of movies by year in DESC order
