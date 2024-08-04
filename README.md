
# Spotify EDA and Clustering

## Project Overview

This projects aims to find out the answer to the question "What makes a song popular ?". Furthermore, the project purpose is to understand which artists and genres are performing highly based on current 'track popularity'. From this, the project will try to identify patterns that set them apart from unpopular songs. This is based of a smaller sample of the entire Spotify Ecosystem. 

#### Business Problem Definition
Scope of Project
Spotify is the largest music streaming platform in the world. It has revolutionized music listening with various machine learning applications such as NLP and reinforcement learning. Furthermore, it has become a platform for new and upcoming artists to help them reach and engage with an audience. The scope of this project is to determine what makes a particular song popular on spotify? To do so we will explore the relationship between various audio features, genres, artists, and their respective track popularities to try and uncover what truly makes a popular track. More specifically, we’ll be focusing on the best and the worst of the tracks on Spotify to see if there are common themes among the two.

#### Motivation (Why does it matter?)
Discovering what specifically makes songs popular will aid upcoming artists in song production. Given knowledge on how to construct a popular song, they will be able to grow faster on the platform. Additionally, the Spotify marketing team can employ top-funnel strategies with this information to drive more users to the app.

#### Key Features

- Extensive EDA on Spotify track data
- Utilization of Spotify API for data enrichment
- Application of K-means clustering for song categorization
- Analysis of factors influencing track popularity

## Table of Contents

1. [Problem Statement](#problem-statement)
2. [Dataset](#dataset)
3. [Methodology](#methodology)
4. [Key Findings](#key-findings)
5. [API Work](#api-work)
6. [Tools and Technologies](#tools-and-technologies)
7. [Repository Structure](#repository-structure)
8. [How to Use](#how-to-use)
9. [License](#license)

## Problem Statement

The primary goal of this project was to understand "What makes a song popular?" using Spotify's Track Popularity metric. We aimed to leverage this understanding to create value for artists and Spotify stakeholders.

### Research Questions:
- How can Track Popularity be utilized to create value for artists and Spotify stakeholders?
- What variables in the dataset are driving Track Popularity?
- Is there a relationship between specific audio features and Track Popularity?

## Dataset

The dataset combines information from:
1. An existing Kaggle dataset of ~20,000 Spotify tracks
2. Additional data retrieved from the Spotify API (track and artist information)
3. A custom-created blend playlist for team analysis

   ![image](https://github.com/YashvardhanRanawat7/A-Data-Driven-Exploration-of-Spotify-Hits/assets/144149772/3d4de136-b204-4088-a0b3-e6e89a365cce)

## Methodology

1. Data Collection: Utilized Spotify API to enrich existing dataset
2. Data Cleaning and Preprocessing: Handled semi-structured JSON data
3. Exploratory Data Analysis: Analyzed distributions and relationships between variables
4. Feature Engineering: Created new features and normalized Track Popularity
5. Clustering: Applied K-means clustering to categorize songs

## Key Findings

##### Do Certain Audio Features Lead to an Increase in Track Popularity?


<img width="1096" alt="Screenshot 2024-08-04 at 4 09 05 AM" src="https://github.com/user-attachments/assets/3a4ac534-5990-498f-962f-e3fb2e75a289">

##### Exploring Architypes

Given that we can’t determine any relevant features that drive track popularity from the matrix, it might make sense to look at multiple features at once. We'll use our top / bottom artists and genres to explore this idea.

<img width="1111" alt="Screenshot 2024-08-04 at 4 30 07 AM" src="https://github.com/user-attachments/assets/02401fed-14a9-4772-b70f-d2ceb8d3d681">

Interestingly, we see a common trend for the clusters for popular artists and genres. Generally, people enjoy songs that are around the middle range for Valence, Energy, Danceability, and on the lower end for Acousticness, Instrumentalness, Liveliness``.

Furthermore, the unpopular side of genres and artists also seem to share some commonality, but their clusters differ from the popular ones. When plotting the two against each other, you can easily visualize the discrepancy.

##### Clustering
During our data analysis, we encountered a significant challenge, which revolved around the fact that each song was associated with multiple genres, and a considerable number of these genres were found to be redundant. To address this, we are pursuing a clustering approach, which will enable us to achieve the following objectives:

![image](https://github.com/user-attachments/assets/929da730-a419-4bbf-8d82-334ac1e540ba)

- Cluster 0 : It consists of high energy and danceable songs
- Cluster 1 : It consists of songs with high acousticness and low valence so it has songs with a 'sad' vibe
- Cluster 2 : It has the highest mean track popularity and consists of highly danceable songs with high energy
- Cluster 3 : This cluster also has high popularity and an even mix of audio features, it may consist of mainstream songs

![image](https://github.com/user-attachments/assets/4f025669-2477-4062-bf5b-be872c780e50)


## API Work

The project involved extensive work with the Spotify API:

- Set up a developer account and created an app to access the API
- Utilized the Spotipy library for easier API interactions
- Made requests for track, artist, and playlist data
- Implemented token management for continuous data retrieval

For detailed information on the API work, refer to `add_columns.ipynb` and `get_playlist.ipynb` in the repository.

## Tools and Technologies

- Python
- Jupyter Notebook
- Pandas for data manipulation
- Matplotlib and Plotly for visualization
- Scikit-learn for K-means clustering
- Spotify API and Spotipy library


## Repository Structure

- `A01_Decoding_the_Secret_to_Popularity_Spotify.ipynb`: Main analysis notebook
- `add_columns.ipynb`: Script for adding columns using Spotify API data
- `get_playlist.ipynb`: Script for retrieving playlist data
- `images/`: Directory containing visualizations
- `LICENSE`: MIT License file
- `README.md`: This file, containing project information

## How to Use

1. Clone the repository
2. Install required dependencies (list them here or include a `requirements.txt` file)
3. Set up a Spotify Developer account and create an app to get API credentials
4. Run the Jupyter notebooks in the following order:
   - `get_playlist.ipynb` (if you want to analyze a specific playlist)
   - `add_columns.ipynb`
   - `A01_Decoding_the_Secret_to_Popularity_Spotify.ipynb`

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
