# Spotify EDA and Clustering

## Project Overview

This project involves an Exploratory Data Analysis (EDA) and clustering of Spotify track data, aiming to understand what makes a song popular.

### Key Features

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

(Note: Please add your main findings and insights here. You can include key visualizations or summary statistics that highlight your discoveries about what drives track popularity.)

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
