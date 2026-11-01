# AI Problem Design & Student Feedback Classifier

## 1. Problem Statement

Educational institutions receive student feedback about teachers, courses, and learning experiences. Reviewing this feedback manually can be time-consuming.

This project focuses on building an AI system that classifies student feedback into three categories:

* Positive
* Negative
* Neutral

The goal is to help teachers and academic staff understand student opinions more efficiently.

## 2. Target Users

* Teachers
* Educational institutions
* Academic coordinators

## 3. AI Use Case

**Task Type:** Text Classification

**Input:** Student feedback in text format.

**Output:** Positive, Negative, or Neutral.

**Example:**

Input: "The teacher explains concepts clearly."

Expected Output: Positive

## 4. Data Source

The project uses a student feedback sentiment dataset obtained from Hugging Face.

The dataset originally contained 724 records and four columns.

For this project, only the following columns were selected:

* Feedback text
* Sentiment label

Data preprocessing included:

* Removing duplicate records.
* Removing missing values.
* Resetting the dataset index.

After preprocessing, the final dataset contained **639 records and 2 columns**.

## 5. Constraints

* The dataset is relatively small.
* The first version supports English only.
* Sarcasm, spelling mistakes, and mixed sentiments may affect predictions.
* The model may produce incorrect classifications.
* Human review remains important.

## 6. Machine Learning Approach

The prototype uses:

**TF-IDF (Term Frequency-Inverse Document Frequency)**

TF-IDF converts text into numerical features so that a machine learning model can process it.

**Logistic Regression**

Logistic Regression is used to classify feedback into Positive, Negative, and Neutral categories.

The TF-IDF vectorizer uses unigrams and bigrams (`ngram_range=(1, 2)`).

The dataset was divided into:

* Training data: 511 records
* Testing data: 128 records

An 80/20 train-test split was used with stratification.

## 7. Evaluation Results

The model was evaluated using accuracy, precision, recall, F1-score, and a confusion matrix.

**Model Accuracy: 59.38%**

**Baseline Accuracy: 59.38%**

### Classification Report

| Sentiment | Precision | Recall | F1-Score |
| --------- | --------: | -----: | -------: |
| Negative  |      0.43 |   0.44 |     0.44 |
| Neutral   |      0.22 |   0.16 |     0.19 |
| Positive  |      0.73 |   0.79 |     0.76 |

**Weighted F1-Score:** 0.58

The model achieved approximately 59.38% accuracy. It performed better on positive feedback than on negative and neutral feedback.

The model did not meaningfully outperform the majority-class baseline. Therefore, the initial 80% accuracy target was not achieved.

## 8. Example Inputs and Outputs

The following examples were tested using the trained model:

| Input Feedback                                | Predicted Sentiment |
| --------------------------------------------- | ------------------- |
| The teacher explains everything very clearly. | Positive            |
| The lectures are boring and confusing.        | Neutral             |
| The class starts at 9 AM.                     | Positive            |

These examples demonstrate that the model can generate predictions, but some predictions may be incorrect.

## 9. Project Limitations

* The model has limited accuracy.
* Neutral feedback is particularly difficult for the current model.
* The dataset is relatively small.
* The model may misunderstand context or sentence meaning.
* Predictions should not be treated as completely reliable.

## 10. Expected Outcome

The project demonstrates a basic machine learning prototype that classifies student feedback into sentiment categories.

It provides a starting point for understanding text preprocessing, feature extraction, model training, and evaluation.

## 11. Project Status

* Problem definition: Completed
* Dataset preprocessing: Completed
* Train-test split: Completed
* TF-IDF feature extraction: Completed
* Logistic Regression model training: Completed
* Model evaluation: Completed
* Example predictions: Completed
* GitHub documentation: In progress

## 12. Future Improvements

* Support Urdu and Roman Urdu.
* Use a larger and more diverse dataset.
* Improve classification performance.
* Build a simple web interface.
* Evaluate the model on additional feedback examples.

## 13. Documentation

**Task 1 – AI Problem Design Document:**

[View Problem Design Document](https://docs.google.com/document/d/1n7dkTUNNrBXQhRPU_8jUFWjfHNOKqb0YNJETopXir3o/edit?usp=sharing)

---

**Project Type:** Machine Learning – Text Classification

**Technologies:** Python, Pandas, Scikit-learn, TF-IDF, Logistic Regression, Google Colab


* Support Urdu and Roman Urdu.
* Use a larger dataset.
* Build a simple web interface.
* Evaluate the model on more diverse feedback.
