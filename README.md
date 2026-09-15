# Bellabeat Data Analysis Case Study
**Google Data Analytics Professional Certificate Capstone Project**

---

## 📌 Executive Summary
Bellabeat is a high-tech manufacturer of health-focused products for women. This case study analyzes smart device fitness data from FitBit users to gain insights into consumer usage patterns and uncover potential growth opportunities for Bellabeat's product line, specifically the **Bellabeat Leaf** wellness tracker and **Bellabeat App**.

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

---

## 💡 Strategic Marketing Recommendations
1. **Personalized Inactivity Alerts:** Implement gentle haptic nudges via the Bellabeat App to encourage short movement breaks during prolonged sedentary periods (>1 hour).
2. **Bedtime Routine & Sleep Hygiene:** Introduce bedtime notifications 30 minutes before target sleep times to help reduce the ~39-minute awake time in bed.
3. **Progressive Step Goals:** Set adaptive daily step targets starting at 8,000 steps before scaling up to 10,000 to improve user engagement without causing burnout.
4. **Battery & Wearability Reminders:** Send push notifications when battery levels drop below 15% to minimize device tracking gaps.

---

## 📂 Project Resources & Documentation
* Project Documentation Files:
* [Google Sheets Interactive Data Workbook](https://docs.google.com/spreadsheets/d/1Hp50CQvi0K8Ycsz_XGn1nn3E744if0QgKkVE92BPqiI/edit?usp=sharing)
   `1_ask.txt` - Business task and stakeholder details.
   `2_prepare.txt` - Data structure, ROCCC analysis, and limitations.
   `3_process.txt` - Data cleaning protocols and transformation logic.
   `4_analyze.txt` - Statistical findings and summary metrics.
