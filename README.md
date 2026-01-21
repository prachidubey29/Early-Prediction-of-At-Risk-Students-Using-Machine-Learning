# Early-Prediction-of-At-Risk-Students-Using-Machine-Learnin
# Early Prediction of At-Risk Students in Distance Learning Using Machine Learning

## Overview

This project presents a structured two-stage machine learning framework designed to support the **early identification of at-risk students** in online and distance learning environments. The goal is to help educators and institutions detect potential disengagement early and enable timely academic interventions that can improve student retention and performance.

The proposed approach integrates:

* **Random Forest (RF)** for feature selection and dimensionality reduction
* **Support Vector Machine (SVM)** for robust classification of students into *at-risk* and *not at-risk* categories

The framework is conceptually grounded and designed to be scalable, interpretable, and adaptable for real-world Learning Management System (LMS) data.

---

## Problem Statement

In distance learning environments, the lack of direct face-to-face interaction makes it difficult to identify students who are struggling. Often, students are only noticed after they perform poorly or drop out. This project addresses this challenge by proposing a machine learning–based early warning system that leverages student data to predict risk proactively.

---

## Key Objectives

* Enable **early detection of at-risk students** using data-driven methods
* Reduce the impact of high-dimensional noisy educational data through effective feature selection
* Improve predictive performance compared to traditional baseline classifiers
* Emphasize **recall** to minimize the risk of missing students who genuinely need support
* Provide a framework that is interpretable and suitable for deployment in real educational systems

---

## Features Considered

The framework assumes data collected from Learning Management Systems (LMS) or Virtual Learning Environments (VLE), including:

### Demographic Features

* Age
* Gender
* Prior education background
* Socioeconomic indicators
* Disability status

### Academic Features

* Previous GPA
* Quiz and assignment scores
* Assessment attempts
* Course history

### Behavioral / Engagement Features

* Login frequency
* Time spent on platform
* Resource views
* Video watch duration
* Forum participation
* Assignment submission patterns
* Activity trends over time

These features together provide a holistic view of student engagement and performance.

---

## Methodology

The proposed system follows a clear machine learning pipeline:

### 1. Data Preparation

* Data cleaning (handling duplicates, inconsistent records)
* Missing value imputation
* Normalization (for SVM compatibility)
* Encoding categorical variables
* Temporal feature engineering (capturing activity trends)

### 2. Feature Selection (Random Forest)

Random Forest is used to:

* Handle non-linearity and noisy data effectively
* Rank features based on importance scores
* Select the most influential features (top contributors covering ~90% cumulative importance)

This improves interpretability and reduces computational complexity.

### 3. Classification (Support Vector Machine)

The reduced feature set is passed to an SVM classifier, chosen because:

* It performs well on moderate-sized datasets
* It constructs strong decision boundaries
* It generalizes effectively when feature space is optimized

Both linear and RBF kernels are considered conceptually in the framework.

---

## Model Evaluation

The framework was evaluated against baseline models such as:

* Naïve Bayes
* K-Nearest Neighbors (KNN)
* Decision Tree

Performance metrics used:

* **Accuracy** – Overall correctness of predictions
* **Recall** – Ability to correctly identify truly at-risk students (most critical metric)
* **F1-score** – Balance between precision and recall

The hybrid **RF → SVM model consistently outperformed baseline models** across all metrics, demonstrating stronger reliability for early-risk prediction.

---

## Key Contributions

* Proposes a clear, structured, and theoretically grounded ML pipeline for educational risk prediction
* Demonstrates the effectiveness of combining feature selection with classification
* Highlights the importance of recall-focused evaluation in educational applications
* Provides a scalable foundation for future implementation using real LMS datasets

---

## Potential Use Cases

* Early warning systems in universities and online learning platforms
* Academic advising dashboards
* Student retention monitoring tools
* Personalized learning intervention systems

---

## Future Scope

* Implementation on real-world LMS datasets (e.g., Moodle, Coursera, edX data)
* Integration with live dashboards for instructors
* Incorporation of additional features such as sentiment analysis and psychological factors
* Experimentation with deep learning and ensemble approaches


