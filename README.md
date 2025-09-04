# Data Science Club Tasks Submission Repository

![Banner Image](https://img.shields.io/badge/Data%20Science%20Club-Tasks%201%20%26%202-blue?style=for-the-badge&logo=jupyter)  
[![GitHub Repo stars](https://img.shields.io/github/stars/Dheeraj1771/DSC-Tasks-Submission?style=social)](https://github.com/Dheeraj1771/DSC-Tasks-Submission)  

## 🚀 Project Overview
Welcome to my submission for the **Data Science Club's Technical Team Selection Tasks**! This repository contains complete implementations for **Task 1: Data-Driven Insights & Visualization Project** (using NBA Scoring Leaders dataset) and **Task 2: Real-World ML Pipeline Project** (using Bike Sharing Hourly Dataset). 

The projects demonstrate skills in data scraping, cleaning, exploratory data analysis (EDA), visualization, feature engineering, machine learning pipelines, and deriving actionable insights.

- **Repository Structure**:
```bash
├── Task1/                          # Task 1 files
│   ├── TaskI.ipynb                 # Jupyter Notebook for Task 1
│   └── nba_scoring_leaders.csv     # Generated cleaned dataset (optional; code regenerates it)
├── Task2/                          # Task 2 files
│   ├── TaskII.ipynb                # Jupyter Notebook for Task 2
│   └── hour.csv                    # Bike Sharing dataset (download if missing)
├── README.md                       # This file
└── requirements.txt                # Python dependencies for reproducibility
```

This repo is public and ready for review. If you're a fellow club member or recruiter, feel free to star ⭐ or fork it!

## 📋 Tasks Implemented
I completed both tasks as per the club's guidelines, focusing on real-world applicability in sports performance (Task 1) and urban transport (Task 2).

### Task 1: Data-Driven Insights & Visualization Project
- **Dataset**: NBA Annual Scoring Leaders (1992-93 to 2024-25) scraped from Wikipedia.
- **Problem Addressed**: Analyzed scoring trends to provide insights for NBA decision-makers (e.g., coaches, executives) on offensive evolution, player retention, and durability.
- **Features Implemented**:
  -  Data cleaning: Handled scraping errors (HTTP 403), column mapping, year filtering (Year >= 1992), player name cleaning, type conversions.
  - EDA: Computed correlations (e.g., Games Played vs. Total Points: r=0.86).
  - Visualizations: 3 plots (PPG trend line plot, top players bar plot, Games Played vs. Total Points scatter plot) using Seaborn/Matplotlib.
  - Feature Engineering: Added 'Multiple Winner' (boolean for repeat winners) and analyzed patterns (e.g., upward PPG trend with R²=0.15).
  - Actionable Insights: 3 recommendations tied to real-world sports issues (e.g., invest in 3-point training).
- **Bonus/Creative Additions**: Robust error handling (try-except for scraping), tight layout for visualizations, and a conclusion summarizing debugging (e.g., resolved length mismatch errors).
- **Challenges Faced**: Wikipedia scraping blocks (fixed with user-agent headers), dynamic table structures (fixed with column verification/printing), year filter issues (ensured min Year=1992).

### Task 2: Real-World ML Pipeline Project
- **Dataset**: Bike Sharing Hourly Dataset (from UCI ML Repository) for transport domain.
- **Problem Addressed**: Predict hourly bike rentals (regression) to optimize bike redistribution in urban systems, promoting sustainable transport.
- **Features Implemented**:
  - Preprocessing: Imputation (SimpleImputer), scaling (StandardScaler), encoding (OneHotEncoder) via ColumnTransformer.
  - Feature Engineering: Created 'temp_hum_interaction' (temperature * humidity) to capture environmental effects.
  - ML Model: RandomForestRegressor in a scikit-learn Pipeline.
  - Training/Evaluation: 80/20 train-test split, metrics (MSE ~3220.00, R² ~0.93 – values may vary slightly on run).
  - Real-World Explanation: Discussed usefulness for reducing wait times and costs in bike-sharing systems.
- **Bonus/Creative Additions**: Added robustness with optional imputation (even if no missing values), and a note on deploying as a Streamlit app for interactive predictions.
- **Challenges Faced**: Ensuring pipeline handles both numerical/categorical features seamlessly; resolved by placing feature engineering before preprocessing.

## 🛠️ How to Run Locally
Follow these steps to run the projects on your machine. The notebooks are self-contained and reproducible.

### Prerequisites
- Python 3.8+ (tested on 3.12).
- Jupyter Notebook/Lab (install via `pip install notebook`).
- Git (for cloning).

### Installation
1. **Clone the Repository**:
 ```bash
 git clone https://github.com/Dheeraj1771/DSC-Tasks-Submission.git
 cd DSC-Tasks-Submission
```
2. **Set Up Virtual Environment (Recommended)**:
```bash
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
```
3. **Install Dependencies**:
```bash
pip install -r requirements.txt
```
4. **Download Datasets (If Needed)**:
- For Task 1: It generates its dataset via scraping, so no download needed.
- For Task 2: If hour.csv is missing in task2/, download from UCI ML Repository and place it there.

### Running the Notebooks
1. **Start Jupyter**:
```bash
jupyter notebook
```
- (Or jupyter lab for JupyterLab.)

2. **Run Task 1**:
- Open Task1/TaskI.ipynb.
- Run all cells (Ctrl + Shift + Enter or menu: Cell > Run All).
- Outputs: Cleaned CSV, correlations, 3 visualizations, features, insights.
- Expected Runtime: ~10-20 seconds (scraping may take longer on slow connections).

3. **Run Task 2**:
- Open Task2/TaskII.ipynb.
- Run all cells.
- Outputs: Pipeline build, training/evaluation metrics (MSE, R²).
- Expected Runtime: ~1-2 minutes (due to model training on ~17k rows).

## 📝 Credits
- Datasets: Wikipedia (NBA Scoring Leaders), UCI ML Repository (Bike Sharing).
- Libraries: Pandas, Requests, Matplotlib, Seaborn, Scikit-learn.
- Contact: [Your Name] ([your.email@example.com]) – Open to feedback!

If you encounter issues or have questions, open an issue on this repo. Thanks for checking out my submission! 🚀
