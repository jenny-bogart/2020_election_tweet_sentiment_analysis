# 2020 Election Tweet Sentiment Analysis

## Project Overview
This project analyzes tweets involving Joe Biden and Donald Trump surrounding the 2020 election. The tweets are used to identify linguistic patterns, thematic differences, and clustering behavior between political groups. Using natural language processing (NLP) and unsupervised learning techniques, the goal is to identify whether tweet content naturally separates into meaningful political clusters and what language features drive those separations.

## Dataset
I used 2 datasets, hashtag_joebiden and hastag_donaldtrump which were collected using keywords for each candidate. Tweets were collected from 10/15/2020 to 11/18/2020 to include the election day (11/3/2020), the day Joe Biden was announced (11/7/2020) and the days leading up to the election. 

Source: Kaggle - US Election 2020 Tweets: https://www.kaggle.com/datasets/manchunhui/us-election-2020-tweets

## Objectives

My goals of this project are to:
- Clean and preprocess large-scale political tweet data

- Extract meaningful textual features using NLP techniques

- Identify natural clusters within election-related tweets

- Analyze whether clusters align with political affiliation or messaging style

- Interpret the language patterns driving cluster separation


Preprocessing:

- Lowercasing

- Tokenization

- Stopword removal

- Punctuation removal

- Frequency-based filtering

Methodology
1. Text Vectorization:
   - Converted tweets into numerical representations using TF-IDF
   - Emphasized term importance while reducing the impact of commonly used words

2. Feature Scaling
  - Standardized features to ensure balanced clustering performance

3. Clustering
- Applied K-Means clustering to group tweets based on textual similarity
- Evaluated cluster quality using inertia (elbow method)
- Selected an optimal number of clusters based on interpretability and performance

4. Cluster Interpretation
- Examined top terms per cluster
- Compared linguistic patterns across clusters
- Analyzed how political narratives differ in word usage and emphasis

5. Random Forest Modeling
- Predict state election outcome based on tweets
- Examine % support for each candidate

6. Latent Dirichlet Allocation
- Find common phrases/words in positive/negative tweets for each candidate

## Key Insights

1. Linguistic Patterns
- Political discourse naturally clusters based on language style and topic emphasis
- Certain clusters emphasize policy-driven language, while others focus on personal attacks, slogans, or campaign rhetoric
- Biden consistently has a higher sentiment than Trump, but both sentiments spike on election day
  <img width="1188" height="590" alt="image" src="https://github.com/user-attachments/assets/38b7f685-b905-4148-b95e-07325a99900c" />


2. Feature Importance
- High-frequency political terms dominate discourse but are less informative for separation
- TF-IDF weighting helped surface distinctive phrasing and narrative differences
- Clusters were driven more by contextual word usage than by sentiment alone

3. Clustering Behavior
- Clear separation exists even without labeled political affiliation
- Some clusters exhibit overlapping vocabulary, reflecting shared national topics despite ideological differences
- Purely unsupervised methods can still uncover meaningful political structure
- Clusters based on sentiment displayed using PCA
- 
  <img width="565" height="455" alt="image" src="https://github.com/user-attachments/assets/db3c3386-718b-4fda-98a5-1060e4de8fb6" />


## Limitations

- Tweets are short-form text, limiting contextual depth

- Sarcasm and irony are difficult to capture with bag-of-words approaches

- Political affiliation is inferred through language patterns rather than explicit labels

## Future Improvements

- Segment analysis by time (pre-election vs post-election)

- Train a supervised model using cluster labels as features

- Compare TF-IDF with transformer-based embeddings (e.g., BERT)

## Tools & Technologies

- Python

- pandas, numpy

- scikit-learn

NLTK / spaCy

matplotlib / seaborn
