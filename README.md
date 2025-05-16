# Fake-News-Prediction
This project is a machine learning solution that classifies news articles as **Real** or **Fake** using **TF-IDF vectorization** and **Logistic Regression**. It demonstrates strong performance on the "Fake and Real News Dataset". Further, SHAP and LIME explainable AI techniques have been applied to boost the model transparency and interpretability. 

## Dataset Used
- **Name**: Fake and Real News Dataset
- **Source**: [Kaggle Dataset Link](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)
- **Contents**:
  - `Fake.csv`: Contains fake news articles
  - `True.csv`: Contains real news articles

## Features
- Text vectorization using `TfidfVectorizer`
- Binary classification using Logistic Regression
- Model evaluation using accuracy, classification report, and confusion matrix
- Clean pipeline with preprocessing and model training
- Enhanced interpretability through XAI techniques such as SHAP and LIME

## Model Performance
- **Accuracy**: 98.89%
- **Precision**: 0.99
- **Recall**: 0.99
- **F1-score**: 0.99

## Insights
- The dataset is fairly large and balanced.
- Fake and real headlines/articles use noticeably different word patterns—TF-IDF captures that well.
- Logistic Regression is a strong linear classifier for high-dimensional, sparse text.
- An accuracy of 98.9 is achieved with a simple logistic regression model.
- SHAP:
  - Each bar shows how much a particular word (feature) contributes to the model’s output
  - The longer the bar, the more important that word is in making predictions
  - Beeswarm Plot tells the positive and negative impact as well
  - The word "said" appears most and thus contributes most, seems very important in real news
  - "Reuters" is a trusted news source, so this strongly suggests real news
  - "video" May appear more in fake news for clickbait or exaggeration
- LIME:
  - explains one prediction at a time by creating a simpler model around that instance
  - shows what features influenced it the most
  - perfect to understand why a particular article was predicted to be fake or real
