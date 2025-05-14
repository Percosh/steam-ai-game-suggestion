games.csv = https://www.kaggle.com/datasets/fronkongames/steam-games-dataset

Advanced Python Project
Game Recommendation System Using TF-IDF Algorithm

1. Project Overview
This project aims to develop a system that recommends similar games based on the titles users have played or specified.

Recommendations are generated using TF-IDF (Term Frequency-Inverse Document Frequency), based on textual data such as game descriptions, genres, tags, and screenshots.

User feedback (likes or dislikes) is incorporated into the recommendation system to deliver more personalized results.

2. Technologies and Libraries Used
Python: The core programming language for the project.

Tkinter: Used to build the graphical user interface (GUI).

Pandas: Used for data processing and reading CSV files.

Requests: For making API calls to Steam and other web sources.

BeautifulSoup: For HTML cleaning and web scraping.

Scikit-learn: For TF-IDF vectorization and similarity calculations.

Threading and ThreadPoolExecutor: To improve performance by handling API requests and computations concurrently.

3. Main Components of the Code
a. Cache Management
load_cache and save_cache functions store game information in a JSON cache file to reduce API requests and improve performance.

b. Steam API Integration
Retrieves the most recently played games of a user via the Steam API using their Steam ID.

'son_oynanan_oyuna_oneri' function returns the AppIDs of the user's recently played games.

c. Game Data Retrieval
'bilgi_cek' function extracts a game’s description from the Steam store and cleans it of HTML tags.

This data is used to compute similarities between games.

d. Similarity Calculation with TF-IDF
'onerilen_oyun_mantigi' function calculates similarity scores between a specified game and others using TF-IDF vectorization and cosine similarity.

e. User Feedback
Users can mark recommended games as "Liked" or "Disliked."

Feedback is stored in a CSV file and influences future recommendation scores.

f. Price-Performance Recommendation
'onerilen_fiyat_performans_mantigi' function fetches game price data from SteamDB to analyze price-performance.

Recommends the best value-for-money game to the user.

g. User Interface (GUI)
Built with Tkinter to provide an interactive user experience.

Users can enter a game name or Steam ID to receive recommendations.

Recommendations are displayed, and feedback can be provided through the interface.

4. Workflow
Recommendation by Game Name:

The user enters the name of a game.

The system analyzes the similarity between the entered game and others using TF-IDF and provides recommendations.

Recommendation by Steam ID:

The user provides their Steam ID.

The system retrieves the user's recently played games and recommends similar ones.

User Feedback:

The user can indicate whether they liked or disliked the recommended games.

This feedback affects the scoring and improves recommendation accuracy.

Price-Performance Suggestion:

The system identifies the best value-for-money game among the recommendations and suggests it to the user.

5. Conclusion
This project is designed to analyze user preferences and suggest the most suitable games accordingly. With added features like user feedback and price-performance analysis, the recommendation system becomes more adaptive and useful. This allows users to find games that not only match their interests but also fit their budget.
