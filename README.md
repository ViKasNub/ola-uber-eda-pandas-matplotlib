# ola-uber-eda-pandas-matplotlib## 🚖 Project OverviewThis project presents an **Exploratory Data Analysis (EDA)** of ride-booking data inspired by **Ola and Uber**, using **Python, Pandas, and Matplotlib in Google Colab** to uncover business insights, customer behavior patterns, and operational trends.The project focuses on analyzing ride booking data to understand booking outcomes, revenue generation, vehicle performance, demand fluctuations, and payment preferences. This analysis demonstrates practical business intelligence and data analytics techniques used in transportation and mobility platforms.---## 📂 Dataset InformationThe dataset contains booking-related information including:- Booking ID- Booking Status- Vehicle Type- Booking Value- Hour of Booking- Payment MethodThe dataset was loaded and analyzed using **Google Colab** for cloud-based data analysis.---## 🛠 Tech Stack- Python- Pandas- Matplotlib- Google Colab- CSV Data Processing---## 📊 Analysis Performed### Booking Status DistributionThis analysis helps understand booking outcomes such as successful bookings, cancellations, and incomplete rides.```pythondf['Booking_Status'].value_counts().plot(kind='bar')

Business Insight: Helps identify ride completion efficiency and operational issues affecting customer experience.

Revenue Analysis
Analyzed total revenue contribution across different vehicle categories.
df.groupby('Vehicle_Type')['Booking_Value'].sum().sort_values(ascending=False).plot(kind='barh')

Business Insight: Identifies high-performing vehicle categories contributing maximum revenue.

Average Booking Value by Vehicle
Compared average booking values across vehicle types.
df.groupby('Vehicle_Type')['Booking_Value'].mean()

Business Insight: Shows which vehicle segments generate higher per-ride revenue.

Demand by Hour
Analyzed hourly booking demand patterns.
df.groupby('Hour')['Booking_ID'].count().plot(title='Demand by Hour')

Business Insight: Helps identify peak ride demand periods for operational optimization.

Payment Method Preference
Analyzed customer payment preferences.
df['Payment_Method'].value_counts().plot(kind='pie', autopct='%1.1f%%')

Business Insight: Provides insights into customer transaction behavior and payment adoption trends.

💻 Complete Python Code
# ola-uber-eda-pandas-matplotlib# Google Colab Projectimport pandas as pdfrom pandas import read_csvimport matplotlib.pyplot as plt# Load Datasetdf = read_csv('Bookings.csv')# Preview Dataprint(df.head())# Dataset Infoprint(df.info())# Statistical Summaryprint(df.describe())# Booking Status Distributiondf['Booking_Status'].value_counts().plot(kind='bar', title='Booking Status Distribution')plt.show()# Revenue Analysisdf.groupby('Vehicle_Type')['Booking_Value'].sum().sort_values(ascending=False).plot(kind='barh', title='Revenue Analysis')plt.show()# Average Booking Value by Vehicleprint(df.groupby('Vehicle_Type')['Booking_Value'].mean())# Demand by Hourdf.groupby('Hour')['Booking_ID'].count().plot(title='Demand by Hour')plt.show()# Payment Method Preferencedf['Payment_Method'].value_counts().plot(kind='pie', autopct='%1.1f%%')plt.show()

📌 Key Business Insights


Booking success and cancellation trends can be analyzed effectively.


Revenue contribution varies significantly across vehicle categories.


Certain vehicle segments generate higher booking value.


Peak booking hours indicate customer demand behavior.


Payment preferences reveal customer transaction habits.



🚀 Skills Demonstrated


Exploratory Data Analysis (EDA)


Python Programming


Pandas Data Analysis


Data Visualization


Business Analytics


Revenue Analysis


Customer Behavior Analysis


Statistical Aggregation


Data Storytelling



🔮 Future Improvements


Interactive dashboard using Power BI / Tableau


Demand forecasting using Machine Learning


Ride cancellation prediction


Customer segmentation


Geospatial hotspot analysis


KPI dashboard for business monitoring



⭐ Project Objective
The objective of this project is to simulate how ride-sharing companies like Ola and Uber can use data analytics to improve operational efficiency, optimize business decisions, and enhance customer experience through data-driven insights.

👨‍💻 Author
Vikas Chavan
Data Analyst | Data Analytics | Python | SQL | AI Enthusiast
