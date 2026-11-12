# AC-Basketball – WNBA Data Analytics & Machine Learning

## Overview

AC-Basketball is a data analytics and machine learning project focused on historical Women's National Basketball Association (WNBA) data.

The project explores historical player, team, coach, awards, and postseason datasets to investigate team playoff qualification and evaluate individual player performance.

It combines data preprocessing, exploratory data analysis, feature engineering, dimensionality reduction, and supervised machine learning to extract insights from basketball statistics.

## Objectives

The project focuses on two main areas:

- **Playoff Qualification Prediction:** Develop and compare machine learning models to estimate the likelihood of teams qualifying for the playoffs based on historical performance.
- **Player Performance Evaluation:** Design an alternative scoring methodology to assess and rank players using statistical performance, awards, playing positions, and season-based weighting.

## Key Features

### 1. Data Exploration and Cleaning

- Explore historical datasets covering players, teams, coaches, awards, and postseason results.
- Analyse missing values and duplicate records.
- Remove irrelevant and redundant attributes.
- Clean and prepare datasets for subsequent processing and modelling.

### 2. Data Preparation and Feature Engineering

- Merge datasets using player and team identifiers.
- Calculate additional statistical indicators, including missed shots and derived performance metrics.
- Prepare numerical and categorical features for machine learning.
- Apply feature transformation and dimensionality reduction techniques, including Principal Component Analysis (PCA).

### 3. Playoff Qualification Prediction

Implement and compare several supervised machine learning algorithms to estimate team playoff qualification probabilities.

**Models explored:**
- Random Forest
- Support Vector Machines (SVM)
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Trees
- Neural Networks

**Modelling workflow:**
- Train models using historical seasons and evaluate them on subsequent seasons.
- Perform hyperparameter optimization with `GridSearchCV`.
- Use 5-fold cross-validation and F1-score as the grid-search optimization metric.
- Evaluate model performance using accuracy, precision, recall, and F1-score.
- Compare predictions across different seasons.
- Generate CSV files containing team identifiers and predicted playoff probabilities.

The prediction workflow also applies a conference-based selection strategy, selecting the four teams with the highest predicted probabilities from each conference.

### 4. Alternative Player Performance Scoring

Develop an alternative scoring methodology to evaluate and rank players based on their historical performance.

The scoring approach considers:

- Individual statistics, including points, rebounds, assists, steals, and blocks.
- Negative performance indicators, such as turnovers and personal fouls.
- Position-specific statistical weights for guards and forwards.
- Individual awards and achievements.
- Season-based weighting to account for performance across multiple years.

The resulting scores are aggregated by player to produce performance rankings.

## Project Structure

```text
AC-Basketball/
│
├── alternative_score/
│   ├── alternative_score.ipynb
│   └── *.csv
│
├── basketballPlayoffs/
│   ├── Season_11/
│   └── *.csv
│
├── cleaned_datasets/
│   └── *_cleaned.csv
│
├── cleaningProcesses/
│   └── *.ipynb
│
├── dataModelsExec/
│   ├── dataModelsExec/
│   │   └── prediction.ipynb
│   ├── kaggle_submission_*.csv
│   └── predictions_*.csv
│
├── dataReduction/
│   ├── featurePrep.ipynb
│   └── featurePrep_with_pca*.csv
│
├── datasetMerger/
│   ├── dataMerging.ipynb
│   └── df_merge.csv
│
├── docs/
│   └── AC_presentation.pptx
│
├── exploration_dataset/
│   └── *.ipynb
│
├── analise.ipynb
├── cleaning.ipynb
├── data_analysis.ipynb
├── data_cleaning.ipynb
├── model_test.ipynb
└── output.png
```

## Technologies and Libraries

- **Python** – Main programming language.
- **Pandas** – Data manipulation and analysis.
- **NumPy** – Numerical computing.
- **Scikit-learn** – Machine learning, preprocessing, model selection, and evaluation.
- **Matplotlib** – Data visualization.
- **Seaborn** – Statistical data visualization.
- **Jupyter Notebook** – Interactive analysis and experimentation.

## Getting Started

### Prerequisites

- Python 3
- pip
- Jupyter Notebook

### Installation

Clone the repository

Install the required libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

### Running the Notebooks

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebooks to explore the different stages of the project, including data exploration, cleaning, feature engineering, model training, and player performance scoring.

**Note:** Some notebooks rely on relative file paths. Run them from the appropriate project directory to ensure the datasets are found correctly.

## Outputs

The repository includes:

- Raw and cleaned basketball datasets.
- Merged and transformed datasets.
- Feature-prepared datasets, including PCA-based outputs.
- CSV files containing model predictions and playoff probability estimates.
- Aggregated player performance scores and rankings.
- A project presentation in `docs/`.

## Project Scope

AC-Basketball explores how historical basketball data and machine learning techniques can support sports analytics.

By combining predictive modelling with an alternative player evaluation methodology, the project investigates two complementary perspectives: team-level playoff qualification and individual player performance.
