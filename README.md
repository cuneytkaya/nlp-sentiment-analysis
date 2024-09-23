# Sentiment Analysis and Sentiment Modeling for Amazon Reviews

## Project Overview

This project aims to analyze customer reviews of a textile and daily wear product line sold on Amazon. By performing sentiment analysis on customer feedback, the goal is to categorize reviews and build a classification model to better understand customer sentiments. This analysis will help improve product features based on complaints and increase overall sales.

## Dataset Information

The dataset consists of the following features:

- **Review**: The review content written by the customer.
- **Title**: The title or summary of the review.
- **HelpFul**: The number of users who found the review helpful.
- **Star**: The rating given to the product by the customer (1 to 5 stars).

## Project Tasks

### Task 1: Text Pre-processing
1. **Read the Dataset**: Import the dataset from `amazon.xlsx`.
2. **Normalize the Text**: Convert all letters to lowercase.
3. **Remove Punctuation**: Eliminate punctuation marks from the reviews.
4. **Remove Numbers**: Remove any numerical expressions in the reviews.
5. **Remove Stopwords**: Exclude common stopwords that do not contribute significant meaning.
6. **Remove Rare Words**: Exclude words that appear less than 1000 times in the dataset.
7. **Lemmatization**: Apply lemmatization to reduce words to their base form.

### Task 2: Text Visualization
1. **Bar Plot Visualization**:
   - Calculate the frequency of words in the "Review" variable.
   - Filter words with a frequency greater than 500 and visualize them using a bar plot.
2. **WordCloud Visualization**:
   - Combine all words in the "Review" variable into a single string.
   - Generate and visualize a word cloud based on this string.

### Task 3: Sentiment Analysis
1. **Sentiment Intensity Analyzer**:
   - Use the SentimentIntensityAnalyzer from NLTK to compute sentiment scores for each review.
2. **Polarity Scoring**:
   - Calculate polarity scores for the first 10 reviews and classify them as positive (`pos`) or negative (`neg`) based on their compound scores.
   - Label the entire dataset with sentiment labels (`pos` or `neg`).

### Task 4: Preparing Data for Machine Learning
1. **Train-Test Split**: Split the data into training and testing sets.
2. **Vectorization**:
   - Use `TfidfVectorizer` to convert the text data into numerical format suitable for machine learning models.

### Task 5: Modeling with Logistic Regression
1. **Model Training**: Train a logistic regression model using the training data.
2. **Prediction and Evaluation**:
   - Make predictions on the test data and evaluate the model performance using a classification report.
   - Calculate the mean accuracy using cross-validation.
3. **Model Testing with Random Review**:
   - Randomly select a review, transform it using `CountVectorizer`, and predict its sentiment using the logistic regression model.

### Task 6: Modeling with Random Forest
1. **Random Forest Model**: Train a random forest classifier and evaluate its performance using cross-validation.
2. **Model Comparison**: Compare the performance of the random forest model with the logistic regression model.

