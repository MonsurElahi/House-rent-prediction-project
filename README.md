Here's a clean and professional **README** document for your house price prediction script:

---

# 🏠 House Price Prediction using Linear Regression

This Python script predicts the price of a house based on its area (in square feet) using a simple **Linear Regression** model built with **scikit-learn**.

---

## 📌 Features

* Uses a small sample dataset of area vs price.
* Trains a simple linear regression model using `scikit-learn`.
* Accepts user input for the area of a house.
* Predicts and displays the estimated house price in Bangladeshi Taka (৳).

---

## 🛠️ Requirements

Before running the script, make sure the following Python libraries are installed:

```bash
pip install pandas scikit-learn
```

---

## 🧾 Sample Dataset

The script uses the following hardcoded dataset:

| Area (sqft) | Price (৳) |
| ----------- | --------- |
| 1000        | 20000     |
| 1500        | 30000     |
| 2000        | 40000     |
| 2500        | 50000     |
| 3000        | 60000     |

---

## 🚀 How to Run the Script

1. Save the script in a `.py` file, for example: `predict_price.py`

2. Run the script using Python:

   ```bash
   python predict_price.py
   ```

3. Enter the area of the house when prompted. Example:

   ```
   Enter the area of the house in square feet:
   2200
   ```

4. The script will output the predicted price, like:

   ```
   Predicted price: Tk 44,000.00
   Predicted price (rounded): Tk 44,000
   ```

---

## 📦 Code Overview

```python
from sklearn.linear_model import LinearRegression
import pandas as pd
```

* Load required libraries

```python
data = {
    'Area': [1000, 1500, 2000, 2500, 3000],
    'Price': [20000, 30000, 40000, 50000, 60000]
}
df = pd.DataFrame(data)
```

* Create a DataFrame with sample data

```python
X = df[['Area']]
Y = df['Price']
model = LinearRegression()
model.fit(X, Y)
```

* Prepare features and target, then train the model

```python
area = float(input("Enter the area of the house in square feet: \n"))
predicted_price = model.predict([[area]])
```

* Take user input and make prediction

---

## 🧠 Model Used

This script uses **Simple Linear Regression**, which assumes a linear relationship between input (area) and output (price). It's trained using the `fit()` method from `sklearn.linear_model.LinearRegression`.

---

## 📬 Feedback or Questions?

Feel free to reach out or suggest improvements. This is a beginner-friendly demo for learning how machine learning can be used for real-world regression tasks.

---

Let me know if you'd like this as a downloadable file (Markdown, PDF, etc.) or want to include features like plotting or saving the model!
