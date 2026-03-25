# Fraudulent Job Posting Detection

This project analyzes whether characteristics of online job postings can be used to predict the likelihood that a posting is fraudulent.
Developed as part of a University of Chicago Applied Data Science statistical models course.

## Overview

Online job fraud exposes applicants to financial loss, identity theft, and privacy risks. Detecting fraudulent postings is challenging due to limited labeled data and ambiguous signals.

This project builds a structured dataset from raw job postings and aims to develop predictive models to identify fraud.

## Data

* **Source:** Aegean University & Workable
* **Observations:** 17,800 job postings
* **Final Sample:** ~10,600 U.S.-based postings

### Target Variable

* `fraudulent`

  * 1 = Fraudulent
  * 0 = Legitimate

Fraud labels were assigned by platform moderators based on suspicious activity, false information, and user complaints.

### Features

* Job description (text)
* Required education
* Employment type
* Industry
* Screening questions
* Additional job metadata

## Data Preparation

### Missing Data

* Dropped variables with excessive missingness (e.g., `department`)
* Retained missingness as a feature when informative (e.g., missing salary)

### Sample Restriction

* Limited dataset to U.S. postings to reduce variation from:

  * Currency differences
  * Language and formatting inconsistencies

### Feature Engineering

* Converted text fields into numeric features (e.g., description length)
* Standardized continuous variables using z-scores
* Grouped high-cardinality categorical variables into broader categories
* Created dummy variables for categorical features

## Modeling Approach

Models were trained to classify job postings as fraudulent or legitimate.

Typical approaches may include:

* Logistic Regression
* Regularized models (LASSO / Ridge)
* Tree-based methods (e.g., Random Forest)

Class imbalance and overfitting were key considerations during model development.

## Limitations

* Fraud labels may contain measurement error
* Dataset is platform-specific (Workable), limiting generalizability
* Restricting to U.S. postings reduces sample size

## Future Work

* Incorporate NLP techniques (e.g., TF-IDF, embeddings)
* Explore anomaly detection methods
* Expand to multi-country models with normalized features
* Evaluate model deployment for real-time fraud detection

## Acknowledgments

* University of Chicago Applied Data Science
* Aegean University
* Workable





