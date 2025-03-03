# Keyword-Detection-on-Website
Project Overview

This project aims to classify HTML documents as either containing information about a cancer tumor board or not. The process involves loading, preprocessing, analyzing data, training a classification model, evaluating its performance, and generating predictions.

Dataset

Training Data (train.csv): Contains labeled document IDs and corresponding classifications.

Test Data (test.csv): Contains document IDs without labels.

Keyword Data (keyword2tumor_type.csv): Contains tumor-related keywords used for reference.

HTML Files (htmls/{doc_id}.html): Raw HTML documents corresponding to the document IDs in the dataset.

Steps Performed

1. Data Loading

Read train.csv, test.csv, and keyword2tumor_type.csv.

Load the HTML content for each document ID.

2. Data Preprocessing

Extract raw text from HTML using BeautifulSoup.

Remove scripts, styles, and unwanted tags.

Preprocess text:

Remove non-alphanumeric characters, punctuation, numbers.

Apply stemming and remove stopwords.

3. Exploratory Data Analysis (EDA)

Label Distribution:

Visualized using a bar plot to check class balance.

Text Length Distribution:

Examined how many words each document contains.

Word Cloud:

Generated for tumor board-related text for insights into word frequency.

4. Feature Engineering

Converted raw text into numerical features using TF-IDF Vectorization.

5. Model Training

Used a Random Forest Classifier with 100 estimators.

Split data into 80% training and 20% validation.

6. Model Evaluation

Accuracy: accuracy_score(y_val, y_pred)

Classification Report: Precision, Recall, F1-score breakdown.

Confusion Matrix: Visualized with a heatmap.

ROC AUC Score: Evaluated model's discriminatory power.

ROC Curve: Plotted for performance analysis.

7. Predictions on Test Data

Processed test data similar to training data.

Generated predictions using the trained model.
