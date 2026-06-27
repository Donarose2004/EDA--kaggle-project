Movie Data Analysis & Visualization
This project explores a movies dataset sourced from Kaggle. The analysis involves data cleaning, exploding multi-genre entries, and visualizing the data to uncover trends regarding movie popularity, genre distribution, and voter ratings.

🛠️ Data Cleaning & Preprocessing
The dataset contained complex formats that required preprocessing before visualization. The following steps were performed:

Handling Multi-Genre Rows: The Genre column contained comma-separated strings (e.g., "Action, Sci-Fi, Adventure"). These strings were split into python lists.

Row Explosion: Used Pandas' .explode() method on the Genre column to transform each element of the genre lists into its own row, duplicating the corresponding movie details for accurate genre-specific analysis.

Duplicate Removal: Created a subset of the data (info_pop) containing only Title and Popularity, and dropped duplicate rows to ensure the popularity metrics remained accurate after the genre explosion.

📊 Visualizations & Insights
The script generates three distinct visualizations using matplotlib and seaborn:

1. Top 10 Most Popular Movies
Chart Type: Vertical Bar Plot

Logic: Sorted the unique movie dataset by the Popularity metric in descending order and isolated the top 10 highest-scoring films.

Insight: Clearly identifies which movies hold the highest popularity scores in the dataset.

2. Genre Distribution Percentage
Chart Type: Pie Chart

Logic: Stripped any leading/trailing whitespaces from the exploded Genre column and performed a value count to calculate the exact breakdown of genres.

Insight: Illustrates the market share of each movie genre, highlighting which genres are most frequently produced.

3. Vote Average for Recent Dataset Entries
Chart Type: Horizontal Bar Plot

Logic: Extracted the last 10 movie titles (.tail(10)) from the original dataset and plotted them against their Vote_Average.

Insight: Provides a quick comparative look at user ratings for the final sequence of movies listed in the dataset.
