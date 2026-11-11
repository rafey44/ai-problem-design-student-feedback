# Student Feedback Sentiment Classifier

## 1. Problem Statement

Student feedback provides valuable information about teaching quality and the learning experience. However, manually analyzing large amounts of feedback can be time-consuming.

This project aims to develop a simple Machine Learning prototype that automatically classifies student feedback into three sentiment categories:

- Positive
- Negative
- Neutral

The intended users include teachers, educational institutions, and academic coordinators.

## 2. Methodology

This project uses Natural Language Processing (NLP) and Machine Learning.

**Dataset:**
- Student feedback dataset containing text and sentiment labels.
- 639 records after data cleaning.
- Two columns: text and sentiment.

**Data Preprocessing:**
- Selected required columns.
- Removed missing values.
- Removed duplicate records.

**Feature Extraction:**
- TF-IDF (Term Frequency-Inverse Document Frequency) converts text into numerical features.

**Machine Learning Model:**
- Logistic Regression was used for sentiment classification.
- Dataset was divided into 80% training and 20% testing data.
- Training samples: 511
- Testing samples: 128

## 3. Demo and Results

The prototype was developed and tested using Google Colab.

Example inputs:

| Student Feedback | Predicted Sentiment |
|---|---|
| The teacher explains everything very clearly. | Positive |
| The lectures are boring and confusing. | Neutral |
| The class starts at 9 AM. | Positive |

**Model Evaluation:**

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

The model achieved approximately 56.25% accuracy on the test dataset.

The confusion matrix and classification report are included in the project notebook.

## 4. Limitations

The current prototype has several limitations:

- The dataset is relatively small.
- The model supports English-language feedback only.
- Sarcasm and mixed sentiments can be difficult to classify.
- Some predictions may be incorrect.
- Model performance depends on the quality and diversity of training data.

The prototype should be improved with a larger and more diverse dataset before real-world use.

## 5. Ethical Considerations

- Student feedback should be handled confidentially.
- Personal and identifiable information should not be collected unnecessarily.
- Predictions should not be treated as absolute judgments.
- Human review should be considered before making important educational decisions.
- The model should be evaluated for potential bias and classification errors.

## 6. Technologies Used

- Python
- Google Colab
- Pandas
- Scikit-learn
- TF-IDF
- Logistic Regression
- NLP
- GitHub

## 7. Project Files

- `student_feedback_classifier.ipynb` – Complete implementation and evaluation.
- `dataset.csv` – Cleaned dataset.
- `requirements.txt` – Required Python libraries.
- `README.md` – Project documentation.

## 8. Conclusion

This project demonstrates how Machine Learning and NLP can be used to classify student feedback into positive, negative, and neutral categories.

It provided practical experience in data preprocessing, text feature extraction, model training, evaluation, and developing a basic AI prototype.
