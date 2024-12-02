# Unsupervised Sentiment Analysis of IMDB Reviews Using VADER
## Overview
This project performs unsupervised sentiment analysis on movie reviews scraped from the IMDB website. It leverages the VADER (Valence Aware Dictionary and sEntiment Reasoner) sentiment analysis tool, which is well-suited for understanding sentiment in text data, especially for social media-like contexts with mixed reviews. The primary goal is to classify and analyze the sentiment of user-generated reviews (positive, neutral, or negative) without requiring labeled datasets.

## Key Features
1. Web Scraping:
The data is collected using a Python-based web scraper tailored for IMDB movie reviews.

2. Sentiment Analysis:
VADER, a lexicon and rule-based model, is used for unsupervised sentiment scoring.

3. Insights:
Outputs include sentiment distributions, individual review scores, and overall movie sentiment trends.

## Key Steps
1. Web Scraping IMDB Reviews:

- Implement a scraper to collect user reviews from specified IMDB movie pages.
- The scraper extracts review text, ratings (if available), and metadata.
- Data is saved in a structured format (e.g., CSV).
2. Data Cleaning:

- Remove irrelevant or non-textual data (e.g., HTML tags, emojis).
- Normalize text by converting to lowercase and handling punctuation.
3. Sentiment Scoring:

- Apply the VADER tool to compute compound, positive, neutral, and negative sentiment scores for each review.
- Categorize sentiment based on thresholds:
  - Compound score > 0.05: Positive
  - Compound score < -0.05: Negative
  - Otherwise: Neutral
4. Analysis and Visualization:

- Calculate sentiment distributions across reviews.
- Generate plots to visualize sentiment trends.
## Project Limitations
1. Model Dependency:
VADER is optimized for short, social media-style text. Accuracy may decrease for long-form movie reviews with complex narratives.

2. Unsupervised Nature:
As this is unsupervised, the model relies on predefined lexicons and cannot account for domain-specific context or unseen words.

3. Data Quality:
The accuracy of sentiment analysis depends heavily on the quality and diversity of the scraped reviews. Noisy or unbalanced datasets can skew results.

4. Language Restriction:
VADER supports only English reviews, limiting the scope for multi-lingual sentiment analysis.
