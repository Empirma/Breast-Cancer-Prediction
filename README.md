# Breast Cancer Prediction Using Machine Learning

A machine learning project that predicts whether a breast tumor is malignant (M) or benign (B) using the Wisconsin Breast Cancer Dataset from Kaggle.

## Overview

This project implements a binary classification model to predict breast cancer diagnosis based on cell nucleus features computed from digitized images of fine needle aspirate (FNA) of breast masses.  The dataset contains measurements of 30 features describing characteristics of cell nuclei present in the images.

## Objectives

- Download and preprocess the Wisconsin Breast Cancer Dataset
- Perform exploratory data analysis (EDA)
- Apply label encoding to categorical variables
- Train machine learning models for binary classification
- Predict breast cancer diagnosis (Malignant or Benign)

## Dataset

**Source:** [Breast Cancer Wisconsin (Diagnostic) Data Set](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)

**Dataset Statistics:**
- **569 samples** (212 Malignant, 357 Benign)
- **32 features** (30 real-valued features + ID + diagnosis)
- **License:** CC-BY-NC-SA-4.0

**Features include:**
- Radius (mean of distances from center to points on the perimeter)
- Texture (standard deviation of gray-scale values)
- Perimeter
- Area
- Smoothness (local variation in radius lengths)
- Compactness (perimeter² / area - 1.0)
- Concavity (severity of concave portions of the contour)
- Concave points (number of concave portions of the contour)
- Symmetry
- Fractal dimension ("coastline approximation" - 1)

Each feature has three measurements:  mean, standard error (se), and worst (largest value).

## Technologies Used

- **Python 3**
- **Pandas** - Data manipulation and analysis
- **Seaborn** - Data visualization
- **Scikit-learn** - Machine learning algorithms
- **Jupyter Notebook** - Interactive development environment
- **Kaggle API** - Dataset download

## Project Structure

```
breast-cancer-prediction/
│
├── breast_cancer_prediction.ipynb    # Main Jupyter notebook
└── README.md                          # Project documentation
```

## Getting Started

### Prerequisites

```bash
pip install pandas seaborn scikit-learn kaggle
```

### Kaggle API Setup

1. Create a Kaggle account at [kaggle.com](https://www.kaggle.com/)
2. Go to your account settings and create a new API token
3. Download the `kaggle.json` file
4. Place it in `~/.kaggle/` directory (Linux/Mac) or `C:\Users\<Username>\.kaggle\` (Windows)

### Running the Project

1. Clone this repository: 
```bash
git clone https://github.com/Empirma/Breast-Cancer-Prediction.git
cd Breast-Cancer-Prediction
```

2. Open the Jupyter notebook:
```bash
jupyter notebook breast_cancer_prediction. ipynb
```

3. Update the Kaggle API credentials in the notebook (if not using kaggle. json):
```python
os.environ['KAGGLE_USERNAME'] = 'your_username'
os.environ['KAGGLE_KEY'] = 'your_api_key'
```

4. Run all cells sequentially

## Workflow

1. **Import Libraries** - Load necessary Python packages
2. **Download Dataset** - Fetch data from Kaggle using the Kaggle API
3. **Load & Explore Data** - Read CSV file and perform initial data exploration
4. **Data Preprocessing** - Handle missing values and clean the dataset
5. **Label Encoding** - Convert categorical diagnosis labels to numerical values
6. **Model Training** - Train machine learning classifiers
7. **Evaluation** - Assess model performance using appropriate metrics

## Key Findings

- Dataset contains **569 samples** with **32 columns**
- **357 Benign (B)** cases
- **212 Malignant (M)** cases
- One column (`Unnamed: 32`) contains only null values and is dropped during preprocessing
- Final dataset:  **569 rows × 32 columns** (after cleanup)
