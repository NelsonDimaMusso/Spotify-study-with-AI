# Spotify-study-with-AI

# Predictive Analysis of Spotify Data: Music Genre Classification and Popularity Prediction using KNN Algorithm

![Spotify Logo](https://upload.wikimedia.org/wikipedia/commons/1/19/Spotify_logo_without_text.svg)

## Table of Contents
1. [Introduction](#introduction)
2. [Related Works](#related-works)
3. [Methods](#methods)
4. [Dataset Preparation](#dataset-preparation)
5. [Model Implementation](#model-implementation)
6. [Model Validation](#model-validation)
7. [Analysis & Recommendations](#analysis--recommendations)
8. [Conclusion](#conclusion)
9. [References](#references)
10. [Graphics](#graphics)

## Introduction

### Abstract
This study explores the application of machine learning techniques on Spotify audio data to address two distinct problems:
1. Music genre classification
2. Song popularity prediction

We implemented two models based on the k-nearest neighbors (KNN) algorithm, achieving satisfactory accuracy for genre classification and moderate predictive capability for popularity prediction.

### Context
Digital music platforms like Spotify accumulate massive amounts of data on song audio characteristics, representing an exceptional opportunity to analyze musical trends and develop predictive models.

### Aim
Develop machine learning models capable of analyzing Spotify songs' audio characteristics to:
1. Effectively classify musical genres
2. Predict track popularity

## Related Works
Key findings from previous research:
- Tzanetakis and Cook (2002): 61% accuracy across 10 genres
- Valle et al. (2021): 78% accuracy with ensemble algorithms
- Martín-Gutiérrez et al. (2020): Random Forest generally outperformed KNN for popularity prediction
- Johnson and Tsai (2021): Significant performance improvements after data standardization

## Methods

### Data Description
The dataset includes various audio features extracted by Spotify:
- **Numerical features**: danceability, energy, key, loudness, mode, speechiness, acousticness, instrumentalness, liveness, valence, tempo, time_signature, duration_ms
- **Target variables**: track_genre (classification), popularity (regression)

### Machine Learning Techniques
We chose KNN algorithm because of:
- Conceptual simplicity and ease of implementation
- Natural ability to handle multi-class problems
- Adaptability to continuous data
- Versatility for both classification and regression

## Dataset Preparation

### Data Exploration
Key findings:
- Popularity shows complex distribution with multiple peaks
- Audio features show varied distributions (normal, skewed, bimodal)
- Notable correlations between features (e.g., energy & loudness: 0.76)

### Preprocessing Steps
1. Handling missing values
2. Selection of 13 most relevant numerical features
3. Limitation to 10 most frequent genres
4. Train-test split (80%-20%)
5. Feature normalization (StandardScaler)
6. Genre encoding (LabelEncoder)

## Model Implementation

### KNN for Genre Classification
- Optimal k value: 59
- Best distance metric: Manhattan (accuracy: 0.4636)
- Trained on 8,000 samples, tested on 2,000

### KNN for Popularity Prediction
- Optimal k value: 11
- Distance metric: Euclidean (MSE: 415.8460)
- Trained on 8,000 samples, tested on 2,000

## Model Validation

### Classification Results
- Overall accuracy: 0.4605 (vs 0.1 random baseline)
- Best performing genres:
  - Ambient (F1: 0.75)
  - Black-metal (F1: 0.76)
- Most confused genres: alternative and alt-rock

### Regression Results
- R²: 0.1508
- RMSE: 20.3923
- Systematic prediction bias (underestimates high popularity, overestimates low)

## Analysis & Recommendations

### Key Findings
- Audio features can predict genre but struggle with similar genres
- Popularity is weakly correlated with audio features alone
- Optimal k differs significantly between tasks (59 vs 11)

### Recommendations
1. Methodological improvements:
   - Feature selection/weighting
   - Ensemble methods
   - Hierarchical classification
2. Dataset enhancements:
   - Additional non-audio features
   - More balanced genre taxonomy
3. Practical applications:
   - Hybrid approaches for recommendation systems
   - Focus on danceability/acousticness for broader appeal

## Conclusion
- KNN provides a valuable entry point for music analysis
- Achieved moderate success in genre classification (46.05%)
- Limited success in popularity prediction (R² 0.1508)
- Future work should explore more sophisticated algorithms and additional features

## References
- Tzanetakis & Cook (2002)
- Valle et al. (2021)
- Martín-Gutiérrez et al. (2020)
- Johnson & Tsai (2021)

## Graphics
All graphics and visualizations are available in the project repository. Key figures include:
- Feature distributions
- Correlation matrix
- Confusion matrix
- Prediction vs actual plots
- Residual analysis

![image](https://github.com/user-attachments/assets/b04cc252-8e19-45de-b9e7-46567377307e)
![image](https://github.com/user-attachments/assets/059e7443-d930-4e0e-a978-4758281db81f)
![image](https://github.com/user-attachments/assets/69f54808-dc64-4a72-9123-c7b1960c2b2a)
![image](https://github.com/user-attachments/assets/d7d57263-a63b-4851-bcbc-7a1153367554)
![image](https://github.com/user-attachments/assets/92b4df7f-0e36-4006-9919-17bdd6dba819)
![image](https://github.com/user-attachments/assets/9ae61bd4-5147-411f-8bd8-0b257e0b0d3c)
![image](https://github.com/user-attachments/assets/dd121988-c0af-4e4c-9019-1dad332c8f83)
![image](https://github.com/user-attachments/assets/3378e9f4-01dd-4c0b-83a0-49d2387ad3b4)
![image](https://github.com/user-attachments/assets/3518681c-79e8-4856-bedb-6bddc4fcd29e)
![image](https://github.com/user-attachments/assets/12b688f1-8b14-4412-88da-bc512f3860f2)
![image](https://github.com/user-attachments/assets/d906cab5-a059-4cdd-843a-a62a1624f0e0)


---

**Created by:**   
EHONGO DIMA--MUSSO Nelson
