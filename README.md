# Netflix-Data-Cleaning-Analysis-and-Visualization
## Project Report: Exploratory Data Analysis of Netflix Content

## 1. Introduction

This project presents an Exploratory Data Analysis (EDA) of a Netflix content dataset. The primary objective is to understand the composition of Netflix's library, identify trends in content acquisition, analyze geographical contributions, explore rating distributions, and discover popular genres and creators. These insights can inform content strategy and audience targeting.

## 2. Dataset Overview and Preparation

The analysis begins by loading the `netflix1.csv` dataset. Key steps in data preparation include:

* **Loading Data**: The dataset is loaded into a Pandas DataFrame.
* **Initial Inspection**: Displaying the first few rows (`db.head()`) and checking data types and non-null counts (`db.info()`) provides a foundational understanding of the dataset's structure, including columns like `type`, `title`, `director`, `country`, `date_added`, `release_year`, `rating`, `duration`, and `listed_in`.
* **Handling Missing Values**: Missing values in `director`, `country`, and `rating` are identified and addressed by filling them with 'Not Given' to maintain data integrity for analysis. Similarly, `listed_in` (genres) are handled.
* **Date Conversion**: The `date_added` column is converted to datetime objects to facilitate time-series analysis of content additions.
* **Feature Engineering**: New columns like `added_year` and `added_month` are extracted from `date_added` to analyze content addition trends over time.

## 3. Exploratory Data Analysis (EDA) - Key Findings

The EDA process uncovers several significant patterns and characteristics of the Netflix content library:

### 3.1 Content Type Distribution

* **Movies Dominate**: The analysis of the `type` column clearly shows that Movies constitute the majority of Netflix's content, significantly outnumbering TV Shows. This indicates a primary strategic focus on film content.
* **Insight**: This distribution highlights Netflix's core offering, suggesting that content acquisition is heavily weighted towards movies.

### 3.2 Geographical Content Contribution

* **Top Contributing Countries**: Analyzing the `country` column reveals that the United States is the overwhelming leader in content production for Netflix. Other significant contributors include India, the United Kingdom, Canada, and France.
* **Insight**: This geographical breakdown indicates Netflix's key content hubs and markets where it sources or produces the most content.

### 3.3 Content Addition Trends Over Time

* **Annual and Monthly Growth**: Plots showing content additions by `added_year` and `added_month` illustrate a notable increase in content, particularly around 2017-2018, with consistent additions throughout the year. There might be slight peaks in certain months for specific content types.
* **Insight**: This trend demonstrates Netflix's aggressive content expansion strategy in recent years.

### 3.4 Content Rating Distribution

* **Prevalent Ratings**: The distribution of `rating` (e.g., `TV-MA`, `TV-14`, `R` for movies, and `TV-MA`, `TV-14` for TV shows) indicates that a significant portion of Netflix's content is geared towards mature and teen audiences.
* **Rating Trends Over Years**: Observing rating trends by `release_year` shows how the types of content ratings have evolved, with high volumes of TV-MA and TV-14 content consistently being added.
* **Insight**: This suggests Netflix caters heavily to an adult and young adult demographic, which informs content development and censorship policies.

### 3.5 Top Directors and Genre Analysis

* **Key Directors**: Identifying directors with the most titles (e.g., Raul Campos, Jan Suter, Marcus Raboy, Jay Karas) reveals recurring collaborations or acquisition patterns with specific creators.
* **Top Genres by Content Type**: Breaking down `listed_in` (genres) by `type` (Movie/TV Show) shows that "Dramas" and "International Movies" are prominent for films, while "Dramas," "International TV Shows," and "Crime TV Shows" are highly popular among series.
* **Insight**: This provides valuable information on content preferences, highlighting globally appealing themes and successful niches within the platform's library.

## 4. Conclusion

This EDA of the Netflix content library provides a clear picture of its strategic focus and growth. Netflix's catalog is predominantly comprised of movies, with the United States leading as the primary content supplier. The platform has experienced significant content expansion, particularly in recent years, maintaining a consistent flow of new titles. Content is largely targeted towards mature and teen audiences, with drama and international content proving to be highly popular across both movies and TV shows. Understanding these dynamics is crucial for content curation, investment decisions, and market positioning.

## 5. Recommendations

Based on these findings, the following recommendations can be made:

* **Content Acquisition**: Continue to invest in diverse "Drama" and "International" content to cater to the demonstrated global demand.
* **Audience Targeting**: Maintain focus on content suitable for TV-MA and TV-14 audiences, as this segment represents a significant portion of the current library.
* **Geographical Expansion**: While the US is dominant, exploring opportunities to expand content partnerships and production in other high-contributing regions could further diversify the library.

## 6. Future Work

Further analysis could include:

* **User Engagement Metrics**: If available, integrate user engagement data (e.g., watch time, completion rates) to correlate with content characteristics.
* **Sentiment Analysis**: Analyze user reviews or social media sentiment related to content to understand audience reception more deeply.
* **Recommendation System Development**: Utilize the insights from popular genres and content types to build or improve a content recommendation engine.
* **Competitive Landscape Analysis**: Compare Netflix's content strategy with other streaming platforms.
