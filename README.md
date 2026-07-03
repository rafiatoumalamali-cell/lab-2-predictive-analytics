

```markdown
# Lab 2: Predictive Analytics with Machine Learning

##  Overview
This repository contains the complete implementation of Lab 2 for Predictive Analytics with Machine Learning. The lab covers three main machine learning tasks using real-world datasets:

1. **Regression**: Predicting taxi tip amounts using NYC Yellow Taxi trip data
2. **Multi-class Classification**: Predicting obesity levels using health and lifestyle data
3. **Unsupervised Clustering**: Discovering hidden patterns in obesity data using K-Means

##  Repository Structure
```
lab-2-predictive-analytics/
├── lab_2_predictive_analytics.ipynb   # Main Jupyter notebook with all code
├── requirements.txt                    # Python package dependencies
└── README.md                          # This file
```

##  Learning Objectives
- Implement a complete machine learning workflow from data loading to model evaluation
- Apply supervised learning techniques (regression & classification)
- Apply unsupervised learning techniques (K-Means clustering)
- Perform feature engineering and preprocessing
- Implement train/validation/test splits
- Diagnose and address overfitting
- Evaluate model performance using appropriate metrics

##  Datasets

### 1. NYC Yellow Taxi Trips (Regression)
- **Source**: NYC Taxi & Limousine Commission
- **Target**: `tip_amount` (continuous)
- **Features**: Trip distance, fare amount, passenger count, location IDs, payment type, etc.
- **Size**: 41,202 rows, 13 columns
- **Goal**: Predict the tip amount a passenger will leave

### 2. Obesity Level Prediction (Classification)
- **Source**: UC Irvine Machine Learning Repository
- **Target**: `NObeyesdad` (7 classes)
- **Classes**: Insufficient_Weight, Normal_Weight, Overweight_Level_I, Overweight_Level_II, Obesity_Type_I, Obesity_Type_II, Obesity_Type_III
- **Features**: Gender, Age, Height, Weight, eating habits, physical activity, etc.
- **Size**: 2,111 rows, 17 columns
- **Goal**: Classify individuals into obesity levels

## 🛠️ Technologies Used
- **Python 3.x**
- **NumPy** - Numerical computing
- **Pandas** - Data manipulation and analysis
- **Scikit-learn** - Machine learning algorithms and preprocessing
- **Matplotlib** - Data visualization
- **Seaborn** - Statistical data visualization
- **Jupyter Lab** - Interactive development environment

## Installation & Setup

### Local Setup
```bash
# Clone the repository
git clone https://github.com/rafiatoumalamali-cell/lab-2-predictive-analytics.git
cd lab-2-predictive-analytics

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate        # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Lab
jupyter lab
```

### Google Colab Setup
1. Open [Google Colab](https://colab.research.google.com/)
2. Upload `lab_2_predictive_analytics.ipynb`
3. Run cells directly (datasets load from URLs automatically)

## Key Results

### Regression (Taxi Tips)
| Model | Train R² | Validation R² | Test R² |
|-------|----------|---------------|---------|
| Linear Regression | 0.0515 | 0.0487 | 0.0512 |
| Random Forest | 0.1289 | 0.0375 | 0.0434 |

### Classification (Obesity Levels)
| Model | Train Accuracy | Validation Accuracy | Test Accuracy |
|-------|---------------|---------------------|---------------|
| Logistic Regression | 92.42% | 87.91% | 89.36% |
| Random Forest | 100.00% | 99.29% | 98.82% |

### Clustering (K-Means)
- **Optimal k**: 7 clusters (matching the 7 true classes)
- **Strongest Cluster**: Cluster 4 (63.6% Obesity_Type_III)
- **Best Separation**: Underweight vs Severe Obesity

## Key Insights

1. **Feature Importance (Obesity)**: BMI is the most important predictor (37.6%), followed by Weight (19.9%)
2. **Tip Prediction**: Taxi tips are difficult to predict from trip characteristics alone (R² < 0.13)
3. **Natural Groupings**: Obesity exists on a continuous spectrum with natural overlap between categories
4. **Model Selection**: Random Forest outperformed linear models for both tasks but showed slight overfitting

## Lab Sections

1. **Section 1 - Regression** (30 pts)
   - Data loading and exploration
   - Preprocessing and feature engineering
   - Train/validation/test split
   - Model training and evaluation
   - Overfitting diagnosis

2. **Section 2 - Classification** (30 pts)
   - Data loading and exploration
   - Preprocessing and feature engineering
   - Stratified train/validation/test split
   - Model training and evaluation
   - Confusion matrix analysis
   - Overfitting diagnosis

3. **Section 3 - Clustering** (20 pts)
   - K-Means implementation
   - Elbow method for k selection
   - Silhouette score analysis
   - PCA visualization
   - Cluster interpretation

4. **Section 4 - Reflection** (15 pts)
   - Supervised vs unsupervised learning
   - Regression vs classification
   - Overfitting strategies

##  Key Takeaways

- **Data Quality Matters**: Clean, well-structured data leads to better model performance
- **Feature Engineering**: Creating meaningful features (BMI, fare_per_mile) significantly impacts results
- **Model Selection**: Complex models (Random Forest) can capture non-linear relationships
- **Overfitting**: Always use validation sets to detect and address overfitting
- **Business Value**: Clustering can reveal patterns even without labeled data

##  Author
**Rafiatou Malam Ali**

##  Course Information
- **Course**: Predictive Analytics with Machine Learning
- **Duration**: 2 weeks (June 18 - June 25, 2026)
- **Due Date**: June 25, 2026|


## License
This project is for educational purposes as part of the Predictive Analytics course.

---
**Last Updated**: 03 July 2026
```

## Additional Files You Might Want to Include:

### .gitignore
```
# Virtual Environment
.venv/
venv/
ENV/
env/

# Jupyter Notebooks
.ipynb_checkpoints/
*.ipynb
!lab_2_predictive_analytics.ipynb

# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python

# Environment variables
.env
*.env

# IDE
.vscode/
.idea/
*.swp
*.swo

# OS
.DS_Store
Thumbs.db
```
