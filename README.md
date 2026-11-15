# Real Estate Price Prediction Using Linear Regression

## Project Overview

This project explores the application of Linear Regression techniques to predict residential property prices using the Bengaluru House Price dataset.

The primary objective is to understand the relationship between property characteristics and housing prices through exploratory data analysis, data preprocessing, correlation analysis, regression modelling, and outlier treatment.

The analysis focuses specifically on properties in **Whitefield, Bengaluru**, and investigates how property size and other housing features influence residential property prices.

## Dataset

The project uses the [Bengaluru House Price Data](https://www.kaggle.com/datasets/amitabhajoy/bengaluru-house-price-data) available on Kaggle.

The original dataset contains **13,320 records and 9 features**, including:

| Feature | Description |
|---|---|
| area_type | Type of property area |
| availability | Property availability status |
| location | Geographical location |
| size | Number of bedrooms or rooms |
| society | Housing society |
| total_sqft | Total property area in square feet |
| bath | Number of bathrooms |
| balcony | Number of balconies |
| price | Property price in lakhs |

For the modelling process, the analysis focuses on properties located in Whitefield, Bengaluru.

## Project Objectives

- Explore and understand the real estate dataset.
- Perform data cleaning and preprocessing.
- Investigate relationships between property characteristics and prices.
- Develop Simple Linear Regression models.
- Identify and handle influential observations using Cook's Distance.
- Compare regression results before and after outlier treatment.
- Develop a Multiple Linear Regression model using Scikit-learn.
- Generate residential property price predictions using the trained model.

## Methodology

### 1. Data Loading and Exploration

- Imported the dataset using Pandas.
- Examined dataset dimensions, variables, and data types.
- Explored property characteristics and price distributions.
- Filtered the dataset to focus on Whitefield properties.

### 2. Data Cleaning and Preprocessing

- Identified missing values.
- Removed incomplete observations where necessary.
- Standardised property size information.
- Converted relevant variables into appropriate numerical formats.
- Prepared the dataset for statistical analysis and regression modelling.

### 3. Exploratory Data Analysis (EDA)

- Examined relationships between property prices and numerical features.
- Conducted correlation analysis.
- Visualised relationships using scatter plots and statistical visualisations.
- Investigated the relationship between property size and price.

### 4. Simple Linear Regression

Developed a Simple Linear Regression model using Statsmodels to examine the relationship between total property area (`total_sqft`) and property price.

The model was assessed using regression statistics, including:

- R-squared
- Regression coefficients
- P-values
- Residual analysis

### 5. Outlier Detection and Treatment

Applied **Cook's Distance** to identify influential observations that could disproportionately affect regression estimates.

The model was subsequently reassessed to examine the impact of outlier treatment on regression performance.

### 6. Multiple Linear Regression

Developed a Multiple Linear Regression model using Scikit-learn.

**Predictor variables:**
- Total square footage (`total_sqft`)
- Number of balconies (`balcony`)

**Target variable:**
- Property price (`price`)

The dataset was divided into training and testing sets using a 70:30 split, with a fixed random state of 10.

## Visualizations

The project incorporates statistical visualizations to explore property characteristics, understand relationships between variables, assess regression assumptions, and evaluate model performance.

### 1. Correlation Matrix

The correlation matrix examines the relationships among numerical variables, including total square footage, number of rooms, bathrooms, balconies, and property prices.

![Correlation Matrix](images/correlation_matrix.png)

**Key observation:** Total square footage demonstrates a strong positive correlation with property price (0.864), suggesting that larger properties generally have higher prices in the analysed dataset.

### 2. Property Price Distribution

The price distribution illustrates how property prices are distributed across the selected Whitefield dataset and helps identify potential skewness and extreme observations.

![Property Price Distribution](images/price_distribution.png)

### 3. Regression Analysis

Regression plots illustrate the relationship between property size and price, while residual plots help assess the model's fit and identify potential patterns in prediction errors.

**Regression Plot**

![Regression Plot](images/regression_plot.png)

**Residual vs. Fitted Plot**

![Residual vs Fitted Plot](images/residual_vs_fitted.png)

### 4. Actual vs. Predicted Prices

The actual-versus-predicted plot compares observed property prices with the prices estimated by the Multiple Linear Regression model.

The closer the observations are to the 45-degree reference line, the closer the predictions are to the actual values.

![Actual vs Predicted Prices](images/actual_vs_predicted.png)

## Results

The final Scikit-learn Multiple Linear Regression model achieved the following result:

| Evaluation Metric | Result |
|---|---:|
| Test-set R² Score | 0.7826 |
| Explained Variance | 78.26% |

The model was also used to generate a sample property price prediction.

**Example input:**
- Total area: 1,500 sq. ft.
- Balconies: 2

**Predicted price:** 96.03 lakh (as represented in the dataset).

The results demonstrate the potential of linear regression for understanding and estimating residential property prices using selected housing characteristics.

## Technologies and Libraries

The project was developed using Python and the following libraries:

| Technology | Application |
|---|---|
| Python | Programming language |
| Pandas | Data manipulation and preprocessing |
| NumPy | Numerical computing |
| Matplotlib | Data visualisation |
| Seaborn | Statistical visualisation |
| Statsmodels | Statistical modelling and regression analysis |
| SciPy | Statistical analysis |
| Scikit-learn | Machine learning and predictive modelling |

## Repository Structure

```text
DSBA_project_Real_Estate_Price_Prediction/
│
├── images/
│   ├── correlation_matrix.png
│   ├── price_distribution.png
│   ├── regression_plot.png
│   ├── residual_vs_fitted.png
│   └── actual_vs_predicted.png
│
├── DSBA_project_Real_Estate_Price_Prediction.ipynb
└── README.md
```

The dataset should be downloaded separately from Kaggle and placed in the project directory before running the notebook.

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/Syeda-Nabila-Akter/DSBA_project_Real_Estate_Price_Prediction.git
```

### 2. Navigate to the Project Directory

```bash
cd DSBA_project_Real_Estate_Price_Prediction
```

### 3. Install the Required Libraries

```bash
pip install pandas numpy matplotlib seaborn statsmodels scipy scikit-learn
```

### 4. Download the Dataset

Download the Bengaluru House Price dataset from [Kaggle](https://www.kaggle.com/datasets/amitabhajoy/bengaluru-house-price-data).

Place the downloaded CSV file in the project directory.

### 5. Open the Jupyter Notebook

```bash
jupyter notebook DSBA_project_Real_Estate_Price_Prediction.ipynb
```

Run the notebook cells sequentially to reproduce the analysis and modelling results.

## Key Learnings

Through this project, I explored:

- Practical applications of statistical analysis and predictive modelling.
- Data cleaning and preprocessing techniques.
- Exploratory data analysis and correlation analysis.
- Simple and Multiple Linear Regression.
- Regression diagnostics and influential observation detection.
- Model evaluation and property price prediction using Scikit-learn.
- The importance of data quality and feature selection in predictive modelling.

## Author

**Syeda Nabila Akter**

Data Science and Business Analytics

[GitHub Profile](https://github.com/Syeda-Nabila-Akter)

[Project Repository](https://github.com/Syeda-Nabila-Akter/DSBA_project_Real_Estate_Price_Prediction)

---

*This project was developed as part of the Data Science and Business Analytics learning journey.*
