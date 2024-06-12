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

# Disaster Response Analyzer

This is a markdown code cell outlining the Disaster Response Analyzer project.

## Installation

Clone the repository:

```bash
git clone https://github.com/Nishieee/Disaster-response-analyzer.git
cd Disaster-response-analyzer
```

Create and activate a virtual environment:

```bash
python3 -m venv env
source env/bin/activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Data Processing Pipeline

The `process_data.py` script implements an ETL (Extract, Transform, Load) pipeline to process and clean the disaster message data. The pipeline performs the following tasks:

- **Extract**: Load raw data from CSV files.
- **Transform**: Clean and preprocess data, including tokenization, lemmatization, and handling missing values.
- **Load**: Store the processed data into a SQLite database for efficient retrieval.

## Machine Learning Pipeline

The `train_classifier.py` script trains and evaluates a machine learning model for classifying disaster messages. The pipeline involves these stages:

- **Feature Engineering**: Transform text data into numerical features using NLP techniques.
- **Model Training**: Train a multi-output classification model to categorize messages into multiple categories (e.g., food, shelter, rescue).
- **Evaluation**: Assess model performance using metrics to ensure accuracy and robustness.

## Usage

To run the web application locally:

```bash
python app/run.py
```

Access the application at [http://localhost:3001/](http://localhost:3001/) in your web browser. The application allows you to input new messages and receive classification results.

