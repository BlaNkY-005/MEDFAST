# MEDFAST – Medicine Recommendation and Disease Prediction System

MEDFAST is an healthcare assistant designed to predict diseases from symptoms and provide personalized medicine, diet, and workout recommendations. The system utilizes machine learning models and structured medical datasets to assist patients and healthcare professionals in early diagnosis and treatment planning.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Machine Learning Models](#machine-learning-models)
- [Repository Structure](#repository-structure)
- [Datasets](#datasets)
- [Notebook Overview](#notebook-overview)
- [Usage Instructions](#usage-instructions)
- [Future Enhancements](#future-enhancements)
- [License](#license)
- [Contact](#contact)

---

## Overview

MEDFAST takes user symptoms as input and provides:
- Predicted disease (using trained ML classifiers)
- Suggested medications
- Recommended diet and workout plans
- Additional description and precautions (planned)

This repository currently includes the complete model-building notebook and a structured dataset, allowing you to reproduce the ML pipeline or integrate it with an application backend.

---

## Features

- Symptom-to-disease prediction using multiple ML algorithms
- Medicine recommendations mapped to diseases
- Data preprocessing with label encoding and imputation
- Feature scaling for selected classifiers
- Dataset contains severity-weighted symptoms and health recommendations
- Fuzzy matching for more flexible symptom input

---

## Machine Learning Models

The following models are evaluated and compared:
- Support Vector Classifier (SVC)
- Random Forest Classifier
- K-Nearest Neighbors (KNN)
- Multinomial Naive Bayes

Evaluation metrics:
- Accuracy
- Precision
- Recall
- F1 Score
- Processing Time (ms)

---

## Repository Structure

```
medfast/
│
├── model/
│   └── MRS.ipynb             # Main Jupyter Notebook for model training and prediction
│
├── dataset/
│   ├── training.csv          # Symptom data with disease labels
│   ├── symptom.csv           # Full list of available symptoms
│   ├── symptom-severity.csv  # Numeric severity for each symptom
│   ├── prediction.csv        # Mapping for model outputs
│   ├── medication.csv        # Medicines mapped to diseases
│   ├── description.csv       # Textual disease descriptions
│   ├── diet.csv              # Recommended diet per disease
│   └── workout.csv           # Exercise/workout tips per disease
│
└── README.md
```

---

## Datasets

- training.csv: Main dataset used to train ML models.
- symptom.csv: Master list of symptoms.
- symptom-severity.csv: Numeric severity scores for symptoms.
- prediction.csv: Maps ML model outputs to disease names.
- medication.csv: Suggests medications for each disease.
- description.csv: Disease definitions and overviews.
- diet.csv: Recommended dietary plans based on condition.
- workout.csv: Suggested workouts or physical activities.

---

## Notebook Overview

The notebook MRS.ipynb includes:
- Dataset loading and cleaning
- Encoding disease labels with LabelEncoder
- Imputing missing values using SimpleImputer
- Feature scaling with MinMaxScaler (for Naive Bayes)
- Model training and accuracy comparison
- Fuzzy symptom matching with fuzzywuzzy
- Prediction logic for mapping symptoms to disease and treatments

---

## Usage Instructions

1. Clone the repository:
   ```
   git clone https://github.com/blanky-005/medfast.git
   cd medfast
   ```

2. Open the notebook:
   - Using Jupyter Notebook:
     ```
     jupyter notebook model/MRS.ipynb
     ```
   - Or use Google Colab by uploading the .ipynb file

3. Run all cells in order:
   - Load the data
   - Train models
   - Input a list of symptoms to get predictions

4. View the predicted disease and retrieve:
   - Recommended medicine
   - Diet and workout plans
   - Symptom severity (optional for scoring)

---

## Future Enhancements

- Web-based interface using Django or Flask
- AR-integrated AI glasses for hands-free symptom recognition
- Multilingual support for rural healthcare
- Real-time chatbot assistant
- Role-based access for doctors and patients

---

## License

This project is licensed under the MIT License. You are free to use, modify, and distribute it with proper attribution.

---

## Contact

Developer: Mohd Hiffzan Abdul Usman  
Email: khnhifzan76@gmail.com  
GitHub: https://github.com/blanky-005  
LinkedIn: https://www.linkedin.com/in/mohd-hiffzan-261474329
