# Ola-Uber-EDA-Pandas-Matplotlib-Analysis

## 🚖 Project Overview
This project presents an Exploratory Data Analysis (EDA) of ride-booking data inspired by Ola and Uber, using Python, Pandas, and Matplotlib in Google Colab to uncover business insights, customer behavior patterns, and operational trends.

The analysis focuses on ride booking data to understand booking outcomes, revenue generation, vehicle performance, demand fluctuations, payment preferences, and cancellation patterns.

---

## 📂 Dataset Information

Dataset features include:
- Booking ID
- Booking Status
- Vehicle Type
- Booking Value
- Hour
- Payment Method

Dataset file: `Data.csv`

---

## 🛠 Tech Stack
- Python
- Pandas
- Matplotlib
- Google Colab
- CSV Data Analysis

---

## 📊 Analysis Performed

### Booking Status Distribution

```python
df['Booking_Status'].value_counts().plot(kind='bar')
```

![Booking Status Distribution](Booking%20Status%20Distribution.png)

---

### Revenue Analysis

```python
df.groupby('Vehicle_Type')['Booking_Value'].sum().sort_values(ascending=False).plot(kind='barh')
```

![Revenue Analysis](Revenue%20Analysis.png)

---

### Average Booking Value by Vehicle

```python
df.groupby('Vehicle_Type')['Booking_Value'].mean()
```

![Average Booking Value by Vehicle](Average%20Booking%20Value%20by%20Vehicle.png)

---

### Demand by Hour

```python
df.groupby('Hour')['Booking_ID'].count().plot(title='Demand by Hour')
```

![Demand by Hour](Demand%20by%20Hour.png)

---

### Payment Method Preference

```python
df['Payment_Method'].value_counts().plot(kind='pie', autopct='%1.1f%%')
```

![Payment Method Preference](Payment%20Method%20Preference.png)

---

### Top Cancellation Reasons

![Top Cancellation Reasons](Top%20Cancellation%20Reasons.png)

---

## 💻 Complete Python Code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv('Data.csv')

print(df.head())
print(df.info())
print(df.describe())

df['Booking_Status'].value_counts().plot(kind='bar')
plt.show()

df.groupby('Vehicle_Type')['Booking_Value'].sum().sort_values(ascending=False).plot(kind='barh')
plt.show()

print(df.groupby('Vehicle_Type')['Booking_Value'].mean())

df.groupby('Hour')['Booking_ID'].count().plot()
plt.show()

df['Payment_Method'].value_counts().plot(kind='pie', autopct='%1.1f%%')
plt.show()
```

---

## 📌 Key Insights
- Booking completion and cancellation trends analysis
- Revenue contribution by vehicle category
- Vehicle-wise average booking value comparison
- Peak demand hour identification
- Customer payment behavior insights
- Cancellation root cause analysis

---

## 🚀 Skills Demonstrated
- Exploratory Data Analysis
- Python
- Pandas
- Matplotlib
- Business Analytics
- Data Visualization
- Customer Behavior Analysis
- Statistical Analysis

---

## ⭐ Project Objective
To analyze ride-sharing booking data and derive business insights that can help optimize operations, improve customer experience, and support data-driven decisions.

---
