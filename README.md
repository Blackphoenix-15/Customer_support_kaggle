# Customer_support_kaggle

# Project Overview
This project aims to build a machine learning model that automatically assigns severity levels (low, medium, high, critical) to customer support tickets based on their textual content. The goal is to help organizations prioritize support tickets effectively, ensuring that critical issues are addressed promptly.

# Dataset
Source
The dataset used in this project was sourced from Kaggle. It contains synthetic data related to customer support tickets.

# Dataset Features
The dataset contains 17 columns:

Ticket ID: Unique identifier for each ticket.
Customer Name: Name of the customer.
Customer Email: Contact email of the customer.
Customer Age: Age of the customer.
Customer Gender: Gender of the customer (Male/Female/Other).
Product Purchased: Product associated with the ticket.
Date of Purchase: Purchase date of the product.
Ticket Type: Type of issue reported (e.g., Technical Issue, Billing Inquiry).
Ticket Subject: Short description of the ticket.
Ticket Description: Detailed description of the issue.
Ticket Status: Status of the ticket (Pending/Closed).
Resolution: Details about how the issue was resolved.
Ticket Priority: Priority level of the ticket (Low/Medium/High/Critical).
Ticket Channel: Channel through which the ticket was raised (Email/Chat/Social Media).
First Response Time: Timestamp of the first response to the ticket.
Time to Resolution: Time taken to resolve the ticket.
Customer Satisfaction Rating: Customer satisfaction score (1–5).
Target Variable
Severity Level: Based on the Ticket Priority and other contextual factors, the goal is to predict the severity level.
# Preprocessing
Steps Taken:
Data Cleaning:
Removed irrelevant columns (Customer Name, Email, etc.).
Handled missing values in Ticket Description and Resolution.
Text Preprocessing:
Tokenization and lowercasing.
Stopword removal and stemming/lemmatization.
Feature Engineering:
Extracted textual features from Ticket Description using TF-IDF.
Created additional features from metadata like Ticket Type and Ticket Priority.
# Model Development
Initial Approach:
TF-IDF + Logistic Regression:
Vectorized the Ticket Description and trained a Logistic Regression model.
Achieved an accuracy of ~26% (not satisfactory).
Refined Approach:
Sentence-BERT + Random Forest:
Used Sentence-BERT to generate embeddings.
Trained a Random Forest Classifier for severity prediction.
This significantly improved the performance.
# Model Evaluation:
# Metrics used for evaluation:

Accuracy: Overall performance of the model.
Precision: Model’s ability to correctly predict each severity class.
Recall: Model’s ability to capture all relevant instances.
F1-Score: Balance between Precision and Recall.

Address class imbalance using oversampling/undersampling techniques.
Fine-tune advanced transformer models like RoBERTa.
Incorporate more features from metadata to improve prediction accuracy.
Hyperparameter tuning for better model performance.
Technologies Used
Python: Main programming language.
Pandas: Data manipulation.
Scikit-learn: Model building and evaluation.
Sentence-BERT: Pre-trained transformer embeddings.
Matplotlib/Seaborn: Data visualization.
