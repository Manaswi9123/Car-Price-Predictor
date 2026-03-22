# Car-Price-Predictor
# 🚗 Car Price Predictor (End-to-End Flask App)

Predicting the resale value of a car involves analyzing multiple variables like brand, age, and usage. This repository features a complete Machine Learning solution—from a messy raw dataset to a polished web application built with **Flask**.

---

## 🛠️ The Tech Stack
* **Data Science:** Python, Pandas, NumPy.
* **Machine Learning:** Scikit-Learn (`LinearRegression`, `OneHotEncoder`, `Pipeline`).
* **Web Backend:** Flask (Python).
* **Frontend:** HTML5, Bootstrap 5, CSS3, JavaScript (AJAX).
* **Serialization:** Pickle.

---

## 🧠 Project Workflow

### 1. Data Cleaning & Engineering (`CarPricePredictor.ipynb`)
* **Data Sanitization:** The raw Quikr dataset was heavily cleaned—removing non-numeric values from years, handling "Ask for Price" entries, and converting kilometers driven into integers.
* **Feature Selection:** Focused on `company`, `name` (model), `year`, `kms_driven`, and `fuel_type`.
* **Pipeline Architecture:** Used Scikit-Learn **Pipelines** and `ColumnTransformer` to bundle preprocessing (One-Hot Encoding) and the Linear Regression model into a single exported file.
* **Optimization:** Ran multiple random train-test splits to find the `random_state` that yielded the highest $R^2$ score (~0.89).

### 2. Flask Web Application (`App.py`)
* **Routing:** Created a Flask server to handle the home page and the `/predict` POST request.
* **Dynamic Loading:** The app dynamically extracts unique car brands and models from the dataset to populate the dropdown menus.
* **AJAX Integration:** Implemented a custom JavaScript `send_data()` function in the frontend. This allows the app to fetch predictions from the server **without reloading the page**, providing a seamless user experience.

---

## 🎨 UI/UX Features
* **Bootstrap Design:** A clean, responsive "card-based" layout.
* **Interactive Dropdowns:** The "Car Model" list updates automatically based on the "Company" selected.
* **Real-time Prediction:** Uses AJAX to display the estimated price instantly on the same page.

---

## 🚀 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git](https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git)
