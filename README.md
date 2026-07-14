Author: Ibeh Doris Chinelo  
Dataset: Netflix Movies and TV Shows 
Date: July, 2026. 

OBJECTIVE 
To explore the Netflix dataset, perform data cleaning to handle missing and invalid values, create 
new features for analysis, and uncover insights through exploratory data analysis and 
visualization. The aim is to understand content trends, audience targeting through ratings, genre 
popularity, geographic production patterns, and the platform’s growth over time. 

DATASET OVERVIEW 
The Netflix dataset contains information about TV shows and movies available on Netflix. Each 
row represents a single title and includes details such as: show_id, type, title, director, cast, 
country, date_added, release_year, rating, duration, listed_in, description. 
Key Details: 
Time Period: Titles released from the 1940s up to 2021, with addition dates from 2008 to 2021 
Data Size: The original dataset had 8,807 rows and 12 columns  
Content Types: The dataset includes both 6,131 Movies and 2,676 TV Shows 
Main Focus: Content metadata including country of production, release year, content rating, 
duration, and genres.

LIBRARIES USED: pandas, matplotlib.pyplot, seaborn 

DATA CLEANING PROCESS 
The dataset was first loaded into Python using pandas. The file loaded properly. After loading 
the data, I checked the structure of the dataset, viewed the first few rows, checked the number of 
rows and columns, reviewed the data types, and identified missing values.  

CLEANING SUMMARY 
Issue Found Action Taken 
Missing director (2,634 rows) was filled with "Unknown" because the data was too large to drop 
Missing cast (825 rows) was filled with "Unknown" because the data was too large to drop 
Missing country (831 rows) was filled with "Unknown" and was excluded from country-specific 
analysis later 
Missing date_added (10 rows) was removed because the data was too small to impact analysis 
Missing rating (4 rows) was removed because it was too small to impact analysis 
Missing duration (3 rows) was removed because it was too small to impact analysis 
Duplicates none was found 
Invalid rating values ("74 min", "84 min", "66 min") was resolved automatically because these 
rows were among those dropped for missing date_added/duration 
date_added was stored as text Converted to datetime 
duration stored as mixed text ("90 min" / "2 Seasons") was splited into two numeric columns: 
duration_minutes (Movies) and duration_seasons (TV Shows) 
Column names was already in clean lowercase snake_case and was confirmed, no changes 
needed 
possible invalid years and duration outliers filtered released_year 1900-2025 and was flagged for 
duration outliers 

FINAL CLEAN DATASET: 8794 rows, 16 columns ( 4 new columns 'duration_num, 
duration_type, duration_minutes, duration_seasons' were added ) 

DATA VISUALIZATION SUMMARY/KEY FINDINGS & KEY INSIGHTS 
Seven virtualization charts were created for better understanding. 
Chart 1: Top 10 Content-Producing Countries  
Key Finding: The United States is the largest producer of Netflix content, followed by India and 
the United Kingdom. 
Key Insight: This shows Netflix’s strategy focuses on English-speaking markets and India, 
which have the biggest subscriber bases. 
Chart 2: Distribution of Movies vs TV Shows  
Key Finding: Movies account for approximately 70% of the catalog, while TV Shows make up 
30%. 
Key Insight: Netflix prioritizes films to quickly grow its library, but still maintains a strong 
collection of series to keep users engaged long-term. 
Chart 3: Content Added to Netflix by Year  
Key Finding: The number of titles added peaked between 2017 and 2019, followed by a sharp 
decline in 2020. 
Key Insight: The peak reflects Netflix’s rapid expansion. The 2020 drop was likely caused by 
COVID-19 production delays. 
Chart 4: Distribution of Release Years  
Key Finding: Most of the content on Netflix was released after 2010. Very little content is from 
before 1990. 
Key Insight: Netflix focuses on modern and recent releases to appeal to current audience 
preferences. 
Chart 5: Distribution of Content Ratings 
Key Finding: TV-MA and TV-14 are the 2 most common ratings. Kids ratings like TV-Y and G 
are very rare. 
Key Insight: Netflix’s catalog is heavily targeted toward Teen and Adult viewers, with limited 
family/kids content. 
Chart 6: Distribution of TV Show Seasons  
Key Finding: The median TV show has only 1 season. Most shows have 1-2 seasons, with a few 
outliers having 10+ seasons. 
Key Insight: Netflix prefers limited series and short-run shows. Long-running shows are 
uncommon on the platform. 
Chart 7: Top 10 Most Common Genres  
Key Finding: The top genres are International Movies, Dramas, and Comedies. Documentaries 
and Action & Adventure also rank high. 
Key Insight: Netflix focuses on Drama and International content to appeal globally, with 
Comedy as a key driver for engagement. 

RECOMMENDATIONS 
1. Content Production & Geography: Increase investment in underrepresented regions like 
Africa, Middle East, and Latin America. 
2. Content Type Balance: Increase original TV Shows and limited series. 
3. Audience Targeting: Develop more Kids and Family-friendly content with ratings TV-Y, G, 
TV-Y7.   
4. Genre Strategy: Continue investing in International Movies, Dramas, and Comedies but also 
expand Documentaries and Reality TV.   
5. Release Strategy: Focus on acquiring and producing recent content from the last 5 years. 
6. TV Show Format: Produce more 1-3 season limited series instead of trying to make 10+ 
season shows. 
7. Post-COVID Recovery: Bring back 2019-level content production rate.
