# 🎵 Spotify Music Analysis: Genre Classification & Popularity Prediction

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.3+-green.svg)](https://pandas.pydata.org/)
[![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A comprehensive machine learning project that analyzes Spotify audio features to classify music genres and predict song popularity using K-Nearest Neighbors (KNN) algorithms.

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [Authors](#authors)

## 🎯 Overview

This project explores the application of machine learning techniques on Spotify audio data to address two distinct problems:

1. **Music Genre Classification**: Automatically classify songs into 10 different genres based on audio features
2. **Song Popularity Prediction**: Predict the popularity score of tracks using audio characteristics

The project uses the K-Nearest Neighbors (KNN) algorithm for both classification and regression tasks, with comprehensive data exploration, preprocessing, and model validation.

## ✨ Features

- **Comprehensive Data Analysis**: 
  - Distribution analysis of audio features and popularity
  - Correlation analysis between different audio characteristics
  - Visualization of relationships between features and popularity

- **Dual ML Approach**:
  - Genre classification with 46% accuracy across 10 genres
  - Popularity prediction with R² score of 0.15

- **Model Optimization**:
  - Hyperparameter tuning for optimal k values
  - Distance metric comparison (Euclidean, Manhattan, Chebyshev)
  - Cross-validation for robust performance evaluation

- **Rich Visualizations**:
  - Feature distributions and correlations
  - Confusion matrices and classification reports
  - Prediction vs. actual value plots
  - Residual analysis for regression model

## 📊 Dataset

The dataset contains Spotify audio features for thousands of songs, including:

### Audio Features
- **Danceability**: How suitable a track is for dancing (0.0-1.0)
- **Energy**: Perceptual measure of intensity (0.0-1.0)
- **Loudness**: Overall volume in decibels (dB)
- **Speechiness**: Presence of spoken words (0.0-1.0)
- **Acousticness**: Measure of acoustic quality (0.0-1.0)
- **Instrumentalness**: Predicts whether a track contains no vocals (0.0-1.0)
- **Liveness**: Detects the presence of an audience (0.0-1.0)
- **Valence**: Musical positivity conveyed by the track (0.0-1.0)
- **Tempo**: Estimated tempo in beats per minute (BPM)
- **Duration**: Track duration in milliseconds

### Target Variables
- **Track Genre**: Musical genre category (10 most frequent genres)
- **Popularity**: Popularity score assigned by Spotify (0-100)

## 🛠️ Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/spotify-music-analysis.git
cd spotify-music-analysis
```

2. **Install required packages**
```bash
pip install -r requirements.txt
```

3. **Required Libraries**
```python
numpy
pandas
matplotlib
seaborn
scikit-learn
warnings
```

## 🚀 Usage

### 1. Data Exploration and Visualization
```bash
python data_exploration.py
```
This script will:
- Load and explore the Spotify dataset
- Generate visualizations of audio features
- Create correlation matrices
- Analyze popularity distributions

### 2. Model Training and Evaluation
```bash
python model_training.py
```
This script will:
- Preprocess the data (normalization, encoding)
- Train KNN models for both classification and regression
- Optimize hyperparameters
- Generate performance metrics and visualizations

### 3. Generated Outputs
The scripts will create several visualization files:
- `popularity_distribution.png`
- `audio_features_distribution.png`
- `correlation_matrix.png`
- `confusion_matrix.png`
- `knn_cv_scores.png`
- `regression_predictions.png`
- `residuals_analysis.png`

## 📈 Results

### Genre Classification Model
- **Overall Accuracy**: 46.05% (significantly better than random 10%)
- **Best Performing Genres**:
  - Ambient: F1-score 0.75
  - Black-metal: F1-score 0.76
- **Optimal Configuration**:
  - k = 59 neighbors
  - Manhattan distance metric
  - Cross-validation score: 0.4636

### Popularity Prediction Model
- **R² Score**: 0.1508 (explains ~15% of variance)
- **RMSE**: 20.39
- **Optimal Configuration**:
  - k = 11 neighbors
  - Euclidean distance metric
  - MSE: 415.85

### Key Insights
- Genres with distinctive audio signatures (ambient, black-metal) are more easily classified
- Audio features alone have limited predictive power for popularity
- Danceability shows positive correlation with popularity
- Acousticness negatively correlates with popularity

## 🔬 Methodology

### Data Preprocessing
1. **Missing Value Handling**: Checked and handled missing values
2. **Feature Selection**: Used 13 numerical audio features
3. **Genre Filtering**: Limited to 10 most frequent genres for balanced classification
4. **Normalization**: Applied StandardScaler to all numerical features
5. **Encoding**: Used LabelEncoder for genre categories

### Model Development
1. **Hyperparameter Optimization**: Systematic search for optimal k values
2. **Distance Metric Comparison**: Evaluated Euclidean, Manhattan, and Chebyshev distances
3. **Cross-Validation**: 5-fold cross-validation for robust performance estimation
4. **Model Validation**: Comprehensive evaluation using multiple metrics

## 🎯 Future Improvements

- **Feature Engineering**: Incorporate additional features like lyrics sentiment or artist popularity
- **Advanced Algorithms**: Explore Random Forest, Gradient Boosting, or Neural Networks
- **Ensemble Methods**: Combine multiple models for better performance
- **Hierarchical Classification**: Implement multi-level genre classification
- **External Factors**: Include marketing data, release timing, and social media metrics

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 👥 Authors

- **EHONGO DIMA--MUSSO Nelson** - *Co-developer and analysis*

## 📚 References

- Tzanetakis, G., & Cook, P. (2002). Musical genre classification of audio signals. IEEE Transactions on Speech and Audio Processing, 10(5), 293-302.
- Valle, R., et al. (2021). Machine learning for music genre classification: An analysis of Spotify audio features. Journal of Computer Science, 17(3), 152-168.
- Martín-Gutiérrez, D., et al. (2020). Predicting song popularity: A comparative study of regression techniques. In Proceedings of the International Conference on Machine Learning Applications, 312-319.

## 🙏 Acknowledgments

- Spotify for providing the audio features dataset
- Scikit-learn community for the excellent machine learning library
- All contributors who helped improve this project

---

⭐ If you found this project helpful, please give it a star on GitHub!
