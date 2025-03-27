# Post-Pandemic Music Trend Analysis

## Overview
This project investigates whether U.S. music listeners shifted from upbeat, high-energy songs to more mellow genres after the COVID-19 pandemic. By analyzing the top 100 streamed tracks on Spotify and Apple Music across 2019, 2022, and 2023, we conducted hypothesis testing to evaluate changes in musical preferences.

Prepared by: Vy Nguyen, Dennis Wu, Kenjee Koh, Hsiang-Han Huang, Becky Wang  

Key findings:
- No statistically significant differences were found between pre- and post-pandemic years.
- Both hypothesis testing and classification methods confirmed the stability in preference for upbeat music.
- Factors like pop culture, emotional regulation, and public settings may influence this consistency.

## Dataset

- **Source:** Spotify & Apple Music APIs (via [Spotipy](https://spotipy.readthedocs.io))  
- **Scope:** Top 100 streamed songs for the U.S. in 2019, 2022, and 2023  
- **Format:** Retrieved via Python API calls and saved as `.csv` files  
- **Key Features:**
  - Danceability, Energy, Acousticness, Valence, Mode, Loudness, Instrumentalness, Tempo, and other audio features
  - Songs are classified ("upbeat" or "sad") based on the scoring system for their audio features

### 📋 Data Dictionary

| Feature           | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| Energy            | Perceived intensity and activity (0.0 to 1.0)                               |
| Valence           | Musical positiveness (0.0 = sad, 1.0 = happy)                               |
| Acousticness      | Confidence that track is acoustic (0.0 to 1.0)                              |
| Loudness          | Overall loudness in decibels                                                |
| Mode              | Type of scale (1 = Major, 0 = Minor)                                        |
| Tempo             | Speed of the track in BPM                                                   |
| Danceability      | Suitability for dancing based on rhythm and tempo                          |
| Speechiness       | Presence of spoken words                                                    |
| Instrumentalness  | Likelihood that the track has no vocals                                     |
| Liveness          | Probability that the track was recorded live                                |
| Key               | Pitch class notation (0 = C, 1 = C#/Db, ..., 11 = B)                        |

## Tools & Methodology Overview

**Languages & Tools:**  
- Python: Spotify API integration, data processing (`pandas`, `spotipy`)  
- Excel: Preprocessing and summary statistics  
- SPSS: T-tests and proportion z-tests for hypothesis testing  

### Statistical Methods

1. **Two-Sample Mean Tests:**  
   Compared Energy, Valence, Acousticness, and Loudness using t-tests across years

2. **Two-Proportion Z-Tests:**  
   Compared Mode and Upbeat classification (binary features) between 2019 vs. 2022 and 2022 vs. 2023

3. **Simplified Classification System:**  
   Converted musical feature values into +1 / 0 / -1 to label each song as “Upbeat” or “Sad”  
   - 2019: 92% Upbeat, 8% Sad  
   - 2022: 94% Upbeat, 6% Sad  
   - 2023: 92% Upbeat, 8% Sad

### 📊 Statistical Results

| Test Type                      | Feature        | Years Compared | p-value  | Conclusion                    |
|-------------------------------|----------------|----------------|----------|-------------------------------|
| Two-Sample T-Test             | Energy         | 2019 vs 2022   | > 0.05   | No significant difference     |
| Two-Sample T-Test             | Valence        | 2019 vs 2022   | > 0.05   | No significant difference     |
| Two-Sample T-Test             | Acousticness   | 2019 vs 2022   | > 0.05   | No significant difference     |
| Two-Sample T-Test             | Loudness       | 2019 vs 2022   | > 0.05   | No significant difference     |
| Two-Proportion Z-Test         | Mode           | 2019 vs 2022   | > 0.05   | No significant difference     |
| Two-Proportion Z-Test         | Upbeat Proportion | 2019 vs 2022 | 0.5794   | No significant difference     |

## Key Deliverables

- Python Script for Spotify API retrieval & processing (.py)
- Final Report (PDF)
- 3 Final datasets for 2019, 2022, and 2023 (.csv)

## What I Learned

- Working with streaming APIs requires proper authentication and robust data cleaning.
- SPSS is highly useful for running clear, interpretable hypothesis tests.
- There's bias in defining musical categories (“upbeat” or "sad") based on a set of thresholds for features.

## What I Plan to Improve

- Incorporate **Natural Language Processing (NLP)** to analyze lyrical sentiment.
- Expand the analysis to include niche or less mainstream songs for more representative insights.
- Develop interactive dashboards (Tableau or Power BI) to better visualize multi-year music trends.

## About Me
Hi, I’m Vy Nguyen and I’m currently pursuing my MS in Business Analytics at UC Irvine. I’m passionate about analytics. Connect with me on [LinkedIn](https://www.linkedin.com/in/vy-ngoc-lan-nguyen).
