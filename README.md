# Disaster Response Analyzer

## Overview
The **Disaster Response Analyzer** is an advanced data processing and machine learning pipeline designed to classify and prioritize emergency messages during disaster events. This system leverages state-of-the-art Natural Language Processing (NLP) techniques and a robust data transformation architecture to ensure efficient and accurate response coordination.

## Table of Contents
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Data Processing Pipeline](#data-processing-pipeline)
- [Machine Learning Pipeline](#machine-learning-pipeline)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Structure
The repository is organized as follows:

```plaintext
Disaster-response-analyzer/
│
├── app/
│   ├── run.py                 # Flask web application entry point
│   ├── templates/
│       ├── master.html        # Main page of the web application
│       └── go.html            # Classification result page
│
├── data/
│   ├── disaster_messages.csv  # Dataset containing disaster messages
│   ├── disaster_categories.csv# Dataset containing message categories
│   ├── process_data.py        # Script for data cleaning and processing
│   └── DisasterResponse.db    # SQLite database for processed data
│
├── models/
│   ├── train_classifier.py    # Script for training the ML model
│   └── classifier.pkl         # Trained ML model
│
├── notebooks/
│   ├── ETL Pipeline Preparation.ipynb   # Jupyter notebook for ETL pipeline exploration
│   └── ML Pipeline Preparation.ipynb    # Jupyter notebook for ML pipeline exploration
│
├── requirements.txt           # Required dependencies for the project
├── README.md                  # Project documentation
└── .gitignore                 # Git ignore file


