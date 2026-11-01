# Financial Sentiment Analysis

## Objective
This project builds an end-to-end text classifier to predict whether real financial news sentences are positive, negative, or neutral. The primary goal is to establish a robust classical NLP pipeline, focusing on text preprocessing and TF-IDF vectorization prior to model training.

## Dataset
* **Source:** Financial Sentiment Analysis.
* **Size:** 5,842 rows.
* **Structure:** Exactly two columns: `Sentence` and `Sentiment` (positive, negative, neutral).

## Methodology & Pipeline
1. **Exploratory Data Analysis (EDA):**
   * Loaded the dataset and visualized the class balance using a bar chart.

2. **Text Preprocessing:**
   * Converted text to lowercase.
   * Utilized Regular Expressions (Regex) to remove stock tickers/symbols (e.g., $ESI), numbers, punctuation, and extra spaces.
   * Removed English stopwords and applied lemmatization using the NLTK library to extract the root meaning of words.

3. **Data Splitting:**
   * Implemented a stratified 80/20 train/test split to ensure the class distribution is preserved across both sets.

4. **Vectorization:**
   * Transformed the cleaned textual data into numerical vectors using `TfidfVectorizer`. The vectorizer was fitted exclusively on the training set to prevent data leakage, and then used to transform both the training and testing sets.

5. **Model Training:**
   * Trained a Baseline Sentiment Model using a `LogisticRegression` classifier on the training vectors.

## Evaluation & Interpretability
* **Metrics:** The model's performance was evaluated on the test set using Accuracy and the weighted F1-Score.
* **Confusion Matrix:** Generated a heatmap to visualize the model's true vs. predicted classifications.
* **Feature Weights Analysis:** Extracted and printed the top 10 words with the most positive weights and the top 10 words with the most negative weights to verify their logical alignment with financial contexts.

## Deliverables
* Jupyter Notebook containing the full code pipeline, required visualizations (class balance, confusion matrix), text cleaning examples, and feature weight printouts.

## Author
**Bayan Marashdeh**