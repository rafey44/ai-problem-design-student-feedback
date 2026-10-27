# AI Problem Design: Student Feedback Classifier

## 1. Problem Statement

Educational institutions receive student feedback about teachers, courses, and learning experiences. Reviewing this feedback manually can be time-consuming.

This project proposes an AI system that classifies student feedback into three categories: Positive, Negative, and Neutral.

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

The initial dataset will contain sample student feedback messages with manually assigned sentiment labels.

Each record will include:

* Feedback text
* Sentiment label

The dataset will be reviewed for reasonable labeling before evaluation.

## 5. Constraints

* The initial dataset will be small.
* The first version will support English only.
* Sarcasm, spelling mistakes, and mixed sentiments may affect predictions.
* The model may produce incorrect classifications.
* Human review will remain important.

## 6. Proposed Approach

A baseline machine learning model using TF-IDF and Logistic Regression will be considered for text classification.

The dataset will be divided into training and testing sets to evaluate performance on unseen examples.

## 7. Success Criteria

The project will aim to:

* Achieve at least 80% accuracy on the held-out test set.
* Report precision, recall, and F1-score for each category.
* Correctly process valid feedback inputs.
* Handle empty or invalid inputs without crashing.
* Document model limitations and evaluation results.

The accuracy target is a goal, not a confirmed result.

## 8. Evaluation Approach

The proposed model will be evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrix

Results will also be compared with a simple baseline classifier.

## 9. Expected Outcome

The expected outcome is a basic AI solution that categorizes student feedback and helps academic staff review opinions more efficiently.

**Project Status:** Problem definition and evaluation plan. Model implementation and testing are pending.

## 10. Documentation

Detailed problem design document: (https://docs.google.com/document/d/1n7dkTUNNrBXQhRPU_8jUFWjfHNOKqb0YNJETopXir3o/edit?usp=sharing)

## 11. Future Improvements

* Support Urdu and Roman Urdu.
* Use a larger dataset.
* Build a simple web interface.
* Evaluate the model on more diverse feedback.
