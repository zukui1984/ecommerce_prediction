# 🛒 E-commerce Customer Purchase Prediction
**ML Zoomcamp 2025 - Midterm Project**

---

## 📑 Table of Contents

- [Problem Description](#-problem-description)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Usage](#-usage)
- [Model Performance](#-model-performance)
- [Key Insights](#-key-insights)
- [Technologies](#-technologies)
- [Deployment](#-deployment)
- [Screenshots](#-screenshots)
- [Future Improvements](#-future-improvements)

---

## 🎯 Problem Description

E-commerce businesses face a critical challenge: **only 2-3% of website visitors make a purchase**. This creates significant opportunities to:

- **Identify high-intent visitors** before they leave the site
- **Personalize user experience** with targeted offers and recommendations
- **Optimize marketing spend** by focusing on likely buyers
- **Reduce cart abandonment** through timely interventions
- **Increase conversion rates** and overall revenue

### Business Impact

For an e-commerce site with:
- **100,000 monthly visitors**
- **$50 average order value**
- **15% baseline conversion rate**

By targeting the top 20% predicted buyers and achieving a 35% conversion rate:
- **Additional 4,000 purchases per month**
- **$200,000 additional monthly revenue**
- **$2.4M additional annual revenue**

This project builds a machine learning system that predicts purchase probability in real-time, allowing businesses to take proactive actions.

---

## 📊 Dataset

**Source:** UCI Machine Learning Repository - [Online Shoppers Purchasing Intention Dataset](https://archive.ics.uci.edu/ml/datasets/Online+Shoppers+Purchasing+Intention+Dataset)

### Dataset Details

| Attribute | Value |
|-----------|-------|
| **Size** | 12,330 sessions |
| **Time Period** | 1 year of data |
| **Features** | 18 original features |
| **Target** | Revenue (Boolean: Purchase/No Purchase) |
| **Class Distribution** | 84.5% No Purchase, 15.5% Purchase |

### Features Description

**Page View Metrics:**
- `Administrative`, `Informational`, `ProductRelated` - Number of pages visited
- `Administrative_Duration`, `Informational_Duration`, `ProductRelated_Duration` - Time spent (seconds)

**Behavioral Metrics:**
- `BounceRates` - Percentage of visitors who enter and leave from the same page
- `ExitRates` - Percentage of pageviews that were the last in the session
- `PageValues` - Average value of pages visited before completing transaction

**Session Information:**
- `Month` - Month of the year
- `OperatingSystems`, `Browser`, `Region`, `TrafficType` - Technical and source info
- `VisitorType` - New Visitor, Returning Visitor, Other
- `Weekend` - Boolean indicating weekend session
- `SpecialDay` - Closeness to special days (e.g., Valentine's, Mother's Day)

### Data Availability

The dataset is included in the `data/` folder. Alternatively, download from:
- **UCI Repository:** https://archive.ics.uci.edu/ml/datasets/Online+Shoppers+Purchasing+Intention+Dataset
- **Kaggle:** https://www.kaggle.com/datasets/roshansharma/online-shoppers-intention

## Project Structure
```
ecommerce-purchase-prediction/
├── data/
│ └── online_shoppers_intention.csv # Dataset
├── screenshots/
│ ├── 01-training-results.png # Training output
│ ├── 02-service-running.png # Flask/Docker running
│ └── 03-prediction-demo.png # API response
├── notebook.ipynb 
├── train.py 
├── predict.py 
├── model.json 
├── dv.pkl 
├── Pipfile 
├── Pipfile.lock
├── Dockerfile 
├── .gitignore 
└── README.md
```
---
## Installation

### Prerequisites

- **Python 3.9+** (Tested on Python 3.13)
- **pipenv** for dependency management
- **Docker** (optional, for containerization)

### Local Setup
1. Clone the repository
git clone https://github.com/yourusername/ecommerce-purchase-prediction.git
cd ecommerce-purchase-prediction

2. Install pipenv (if not already installed)
pip install pipenv

3. Install dependencies
pipenv install

4. Install development dependencies (for Jupyter)
pipenv install --dev

5. Activate virtual environment
pipenv shell


### 1. Explore the Notebook
```python
pipenv run jupyter lab
```

Start Jupyter Lab to see the complete analysis:

