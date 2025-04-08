# BBC News Article Analysis & Summarization System

## Overview
This project analyzes a dataset of 515,000 hotel reviews from across Europe to extract actionable insights about customer satisfaction patterns. Using machine learning techniques, I developed models to predict review scores, identify key factors influencing ratings, and discover geographical patterns in hotel performance.

## Dataset
The dataset contains comprehensive information about hotel reviews:
- **Review content**: Positive and negative reviews with word counts
- **Reviewer details**: Nationality, review history, scoring patterns
- **Hotel information**: Location (latitude/longitude), average scores
- **Trip context**: Tags indicating trip type, duration, traveler type

## Key Technical Implementations

### 1. Data Preprocessing & Feature Engineering
- Cleaned and normalized 515,738 reviews across multiple European countries
- Created sentiment polarity features using TextBlob to quantify review sentiment
- Engineered features from unstructured text data (review length, word counts)
- Extracted stay duration and trip type from tag metadata

### 2. Classification Model
- Implemented Random Forest Classifier to predict high vs. low review scores
- Achieved 76.5% accuracy with sentiment-enhanced features
- Optimized hyperparameters through exhaustive grid search
- Confusion matrix analysis showed balanced precision/recall (0.76/0.78)

### 3. Geospatial Analysis
- Clustered hotels based on geographical proximity using K-means
- Visualized spatial patterns with interactive Folium maps
- Identified regional variations in review scores across Europe
- Correlated location clusters with rating patterns

### 4. Reviewer Nationality Analysis
- Discovered significant variations in scoring patterns across nationalities
- Clustered 50 nationality groups based on average review scores
- Visualized nationality distribution within clusters
- Identified potential cultural biases in review scoring

## Key Findings

1. **Review Content Matters**: 
   - Total review length and sentiment polarity are strong predictors of overall scores
   - Positive word count has 3x more predictive power than negative word count

2. **Trip Context Influences Ratings**:
   - Business travelers rate hotels more critically than leisure travelers
   - Longer stays correlate with more balanced reviews
   - Couples tend to give higher ratings than solo travelers or families

3. **Geographical Patterns**:
   - Clear clustering of highly-rated hotels in specific European regions
   - Hotels in similar locations tend to receive similar ratings
   - Outlier detection identified hotels significantly outperforming their geographical neighbors

4. **Nationality Bias**:
   - Identified systematic variations in how different nationalities rate hotels
   - Some nationality groups consistently give higher/lower scores regardless of hotel quality

## Technologies Used
- **Python**: pandas, numpy, scikit-learn, matplotlib, seaborn
- **Machine Learning**: Random Forest, K-means clustering, Isolation Forest
- **NLP**: TextBlob for sentiment analysis
- **Geospatial**: Folium for interactive maps
- **Visualization**: Matplotlib, Seaborn
