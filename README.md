# Car-Price-Prediction-Regression
This repository contains a comprehensive car price prediction project utilizing regression techniques. It aims to predict car prices with a focus on accuracy and model optimization, leveraging regularization techniques to avoid overfitting. The project is ideal for those looking to understand regression models and improve prediction accuracy.

# 🚗 Car Price Prediction Using Regression Models

## 📌 Project Overview
This project aims to predict car prices based on various attributes such as brand, model year, fuel efficiency, and premium features. Using regression models, the goal is to develop a reliable predictive model that estimates the **Manufacturer’s Suggested Retail Price (MSRP)** with high accuracy.  

Key techniques used:
- **Data Cleaning & Processing**
- **Exploratory Data Analysis (EDA)**
- **Feature Engineering**
- **Multiple Regression Models with Regularization**
- **Model Performance Evaluation**

## 📊 Dataset Description
The dataset contains **28,143 car records** with **8 key attributes**:

| Feature            | Description |
|--------------------|-------------|
| `model_year`       | Manufacturing year of the vehicle |
| `brand`            | Name of the car manufacturer |
| `model`            | Specific car model |
| `type`             | Vehicle classification (SUV, Sedan, Coupe, etc.) |
| `miles_per_gallon` | Fuel efficiency (MPG) |
| `premium_version`  | 1 if the car has a premium variant, else 0 |
| `msrp`             | Car price (target variable) |
| `collection_car`   | 1 if the car is considered a collectible, else 0 |

### 🛠 Data Preprocessing:
- **Handling Missing Values:** Filled or removed where necessary.
- **Outlier Detection & Treatment:** Used **Interquartile Range (IQR) Winsorization** to mitigate extreme values.
- **Feature Encoding:** Converted categorical variables into numerical format.
- **Scaling & Normalization:** Standardized numerical features for better model performance.

---

## 📈 Exploratory Data Analysis (EDA)
Key insights obtained:
- **Price Distributions:** Luxury brands and premium versions tend to have higher MSRPs.
- **Visualization Techniques:** Used **histograms, scatter plots, and box plots** to understand data trends.

---

## 🔮 Regression Models & Performance
### 1️⃣ **Polynomial Regression**
- Applied polynomial transformation to capture nonlinear relationships.
- **Accuracy:**  
  - **Training Score:** **70.93%**  
  - **Testing Score:** **Extremely poor (-5.76 trillion%)** (indicating overfitting and model instability).  

### 2️⃣ **Regularized Regression Models**
To improve performance and prevent overfitting, we applied **Lasso, Ridge, and Elastic Net Regularization**:

| Model                  | Training Accuracy | Testing Accuracy |
|------------------------|-------------------|------------------|
| **Lasso Regression**    | **63.41%**        | **62.68%**       |
| **Ridge Regression**    | **63.40%**        | **62.68%**       |
| **Elastic Net Regression** | **28.30%**      | **28.86%**       |

**Observations:**
- **Lasso & Ridge performed similarly** with moderate accuracy.
- **Elastic Net underperformed**, suggesting that combining L1 and L2 regularization was not beneficial for this dataset.

---

## 🚀 Installation & Usage
### Prerequisites:
Ensure you have **Python 3.x** installed along with the required dependencies.

### 📦 Install Required Libraries:
```bash
pip install pandas numpy matplotlib sklearn

### 🔧 Running the Project:
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/car-price-regression.git
2. Navigate to the project folder:
  ```bash
  cd car-price-regression
3. Open and run the Jupyter Notebook:
  ```bash
jupyter notebook "car_regression.ipynb"


