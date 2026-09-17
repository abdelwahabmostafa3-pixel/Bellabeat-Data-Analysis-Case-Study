# 🚴‍♀️ Bellabeat Smart Device Data Analysis

**Consumer Behavior & Fitness Tracker Case Study**
---

## 📌 Executive Summary
Bellabeat is a high-tech manufacturer of health-focused products for women. This case study analyzes smart device fitness data from FitBit users to gain insights into consumer usage patterns and uncover potential growth opportunities for Bellabeat's product line, specifically the **Bellabeat Leaf** wellness tracker and **Bellabeat App**.

---

## 📊 Interactive Tableau Dashboard
Explore the full interactive visualization dashboard on Tableau Public:  
👉 **[View Bellabeat Interactive Dashboard](https://public.tableau.com/app/profile/mostafa.abdelwahab/viz/BellabeatSmartDeviceFitnessSleepAnalysis/BellabeatSmartDeviceFitnessSleepAnalysis)**

---

## 🛠️ Data Analysis Process

### 1. Ask Phase
* **Business Task:** Analyze FitBit smart device usage data to understand how consumers use non-Bellabeat smart devices and apply these insights to guide marketing strategy for Bellabeat.
* **Key Stakeholders:**
  * Urška Sršen (Co-founder & Chief Creative Officer)
  * Sando Mur (Co-founder & Key Executive)
  * Bellabeat Marketing Analytics Team

### 2. Prepare Phase
* **Data Source:** FitBit Fitness Tracker Data (Public Domain via Kaggle, made available by Mobius).
* **Dataset Scope:** 30 eligible FitBit users who consented to submitting personal tracker data, including minute-level output for physical activity, heart rate, and sleep monitoring.
* **Key Datasets Used:**
  * `dailyActivity_merged.csv` (895 unique daily records)
  * `sleepDay_merged.csv` (411 unique sleep records)

### 3. Process Phase
* **Tools Used:** Google Sheets / Microsoft Excel for data cleaning and transformation.
* **Data Cleaning Steps:**
  * Removed 45 duplicate records in `dailyActivity_merged` and 3 duplicate records in `sleepDay_merged`.
  * Verified date formatting (`YYYY-MM-DD`) and data types for step counts, distance, and activity duration.
  * Checked column integrity: Confirmed `TotalDistance` and `TrackerDistance` are functionally identical.
  * Calculated custom metrics: `TotalTimeInBed - TotalMinutesAsleep` to track latency/awake time in bed.

### 4. Analyze Phase
Key descriptive statistics calculated across user daily activity and sleep records:

| Metric | Average Value | Benchmark / Goal | Key Insight |
| :--- | :--- | :--- | :--- |
| **Daily Steps** | 8,021.9 steps | 10,000 steps | Users average below standard recommended health targets. |
| **Sedentary Time** | 968.6 min (~16.1 hrs) | < 8 hrs | Very high sedentary behavior accounts for most of the day. |
| **Very Active Time** | 21.2 min | 30.0 min | High-intensity workouts make up a very small fraction of routines. |
| **Sleep Duration** | 419.2 min (~7.0 hrs) | 7.0 - 9.0 hrs | Sleep duration meets basic health recommendations. |
| **Time Awake in Bed** | 39.3 min | < 20.0 min | Notable delay in falling asleep or getting out of bed. |

### 5. Share Phase
* **Interactive Visualization:** Designed a multi-chart executive dashboard using Tableau Public.
* **Key Dashboard Visuals:**
  * *Total Steps vs. Calories Burned*: Strong positive linear correlation ($R^2 = 0.338, P < 0.0001$).
  * *Sleep Minutes vs. Time In Bed*: Visualizes user sleep latency (~39.3 min awake in bed).
  * *Average Steps by Weekday*: Identifies lowest activity days (Mondays & Saturdays).

### 6. Act Phase (Marketing & Product Recommendations)
* **Targeted Notifications & Engagement:** Send gentle push notifications on Mondays and Saturdays to encourage light activities, as these days show the lowest average step counts.
* **Smart Sedentary Reminders:** Program the Bellabeat Leaf/Time smart device to issue subtle vibration alerts after 60 consecutive minutes of inactivity during daytime hours.
* **Sleep Hygiene Integration:** Introduce pre-bedtime wind-down alerts and in-app breathing exercises to help reduce the average 39.3 minutes users spend awake in bed.
* **Product Positioning & Marketing:** Emphasize long battery life in marketing campaigns to mitigate data tracking gaps caused by frequent charging cycles.

---

## 📂 Project Resources & Documentation
* **Interactive Workbooks & Dashboards:**
  * 🟢 [Google Sheets Data Workbook](https://docs.google.com/spreadsheets/d/1Hp50CQviOK8Ycsz_XGn1nn3E744ifQ0gKkVE92BPqiI/edit?usp=sharing)
  * 📊 [Tableau Public Interactive Dashboard](https://public.tableau.com/app/profile/mostafa.abdelwahab/viz/BellabeatSmartDeviceFitnessSleepAnalysis/BellabeatSmartDeviceFitnessSleepAnalysis)

* **Phase Documentation Files:**
  * `Ask.1.txt` - Business task and stakeholder details.
  * `Prepare.2.txt` - Data structure, ROCCC analysis, and limitations.
  * `Process.3.txt` - Data cleaning protocols and transformation logic.
  * `Analyze.4.txt` - Statistical findings and summary metrics.
  * `Share.5.txt` - Tableau visualization architecture and chart designs.
  * `Act.6.txt` - Marketing and product recommendations.
