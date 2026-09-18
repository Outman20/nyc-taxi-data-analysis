# 🚕 NYC Taxi Data Analysis

An exploratory data analysis project using NYC Yellow Taxi trip data from January 2025.

The goal of this project is to explore patterns in **taxi demand, trip characteristics, revenue, and tipping behavior** and turn the results into meaningful business insights.

---

## 📌 Business Questions

This project focuses on three main questions:

- 🕐 When is taxi demand highest in New York City?
- 💰 What factors have the strongest relationship with trip revenue?
- 💳 How do passenger count, payment method, and trip characteristics relate to tipping behavior?

---

## 📊 Dataset

The analysis uses the **NYC Yellow Taxi Trip Record Data** for January 2025.

The dataset contains more than **3.4 million taxi trip records** and includes information such as:

- Pickup and drop-off timestamps
- Trip distance
- Passenger count
- Payment type
- Fare amount
- Tip amount
- Total trip amount
- Pickup and drop-off locations

### Data Source

The dataset is provided by the **NYC Taxi & Limousine Commission (TLC)**.

🔗 [NYC TLC Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

---

## 📈 Analysis Workflow

```
Raw Data
   ↓
Data Inspection
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Visualization
   ↓
Relationship Analysis
   ↓
Business Insights
```

---

## 🧹 Data Cleaning

Before performing the analysis, the dataset was inspected for missing values, duplicates, unrealistic values, and outliers.

The following cleaning steps were applied:

- Removed trips with non-positive durations.
- Removed trips with durations above 180 minutes.
- Removed trips with distances above 100 miles.
- Kept negative fare and total amount records in the original dataset, but excluded them from analyses requiring valid positive revenue.
- Restricted the main analysis to trips picked up during January 2025.
- Applied additional outlier filtering for revenue and tip percentage analyses.

The original dataset was kept unchanged, while cleaned datasets were created for analysis.

---

## 🔎 Exploratory Data Analysis

### 🕐 Taxi Demand

Taxi demand was analyzed by:

- Hour of the day
- Day of the week
- Weekday vs. weekend

The analysis shows that demand varies throughout the day, with the highest hourly demand occurring around **18:00**.

### 📏 Trip Distance & Duration

The relationship between trip distance and trip duration was analyzed using Pearson correlation and scatter plots.

A strong positive correlation was found between the two variables (**r = 0.788**), indicating that longer trips generally take more time.

### 💰 Revenue Analysis

The relationship between total trip revenue and different trip characteristics was investigated.

The analysis focused on:

- Trip distance
- Trip duration
- Passenger count

Trip distance showed a stronger relationship with total revenue (**r = 0.885**) than trip duration (**r = 0.750**) or passenger count (**r = 0.053**).

Average revenue also increased substantially as trip distance increased.

### 💳 Tipping Behavior

Tipping behavior was analyzed using tip amount and tip percentage.

The analysis examined:

- Tip percentage vs. fare amount
- Recorded tip rates by payment type
- Credit card vs. cash payments

Among trips with a recorded positive tip, the median tip percentage was approximately **27.4%** after excluding the top 1% of tip percentages.

Recorded tips were much more common for credit card payments than cash payments. However, this reflects **recorded tip amounts**, and cash tips may not be fully captured in the dataset.

---

## 💡 Key Findings

- 🕐 **Demand:** Taxi demand is highest around **18:00**, while demand is lowest during the early morning.
- 📏 **Revenue:** Trip distance has a stronger relationship with total revenue than trip duration or passenger count.
- 💰 **Distance & Revenue:** Average revenue increases substantially as trip distance increases.
- 💳 **Tipping:** Recorded tipping behavior differs strongly between credit card and cash payments.
- 💵 **Tip Percentage:** The median recorded tip percentage is approximately **27.4%** among positive-tip trips after outlier filtering.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas**
- **Matplotlib**
- **Jupyter Notebook**
- **Parquet**

---

## 📁 Project Structure

```text
nyc-taxi-data-analysis/
│
├── data/
│   └── yellow_tripdata_2025-01.parquet
│
├── notebooks/
│   └── nyc_taxi_analysis.ipynb
│
└── README.md
```

---

## 🎯 Conclusion

This project demonstrates how real-world transportation data can be cleaned, explored, and analyzed to identify patterns in demand, revenue, and tipping behavior.
The analysis also highlights the importance of handling missing values, anomalous records, and extreme outliers when working with large real world datasets.

---

## 👤 About

This project is part of my Data Science portfolio, where I am building practical projects to develop my skills in data analysis, SQL, Python, and data visualization.