# COVID-19 Twitter Sentiment Analysis & Classification

This repository features a comprehensive Natural Language Processing (NLP) pipeline designed to classify public sentiment during the COVID-19 pandemic using Twitter data. The project transitions from raw social media data to structured insights using statistical analysis and machine learning.

## 📊 Dataset Overview
The project utilizes the **Corona NLP Dataset**, which consists of two primary files:
- `Corona_NLP_train.csv`: Primary training data.
- `Corona_NLP_test.csv`: Independent test set for final evaluation.

**Data Attributes:**
- **UserName/ScreenName:** Anonymized identifiers.
- **Location:** Geographical origin of the tweet (top locations include United States, London, and New York).
- **TweetAt:** Date of the tweet.
- **OriginalTweet:** The raw text content.
- **Sentiment:** The target label (5-class: Extremely Positive, Positive, Neutral, Negative, Extremely Negative).

## 🛠️ Technical Workflow

### 1. Data Integration & Audit
- Merged training and test sets to ensure consistent preprocessing across all 44,955 records.
- Performed a null-value audit, identifying that while text and labels are complete, approximately 21% of tweets lack "Location" data.

### 2. Exploratory Data Analysis (EDA)
- **Sentiment Distribution:** Visualized using bar charts to identify class frequency. "Positive" and "Negative" sentiments were found to be the most prevalent.
- **Geospatial Analysis:** Analyzed top tweeting locations to understand the global spread of the conversation.

### 3. Text Preprocessing (NLP Pipeline)
To prepare the noisy Twitter data for modeling, the following steps were implemented:
- **Cleaning:** Removal of URLs, HTML entities, and special characters.
- **Normalization:** Converting all text to lowercase.
- **Stopword Filtering:** Leveraging NLTK to remove non-informative words.

### 4. Advanced Visualization
- **t-SNE Dimensionality Reduction:** Visualized high-dimensional text data in 2D space to observe natural clustering of sentiments.
- **Correlation Mapping:** Used Seaborn heatmaps to examine relationships between different features.

## 🚀 Installation & Usage

### Prerequisites
- Python 3.8+
- Jupyter Notebook or Google Colab

