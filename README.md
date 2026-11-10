# Cyclistic Bike-Share Analysis: Case Study 1

## 📌 Project Overview
This case study is part of the Google Data Analytics Professional Certificate capstone project. In this project, I assume the role of a junior data analyst working on the marketing analyst team at **Cyclistic**, a fictional bike-share company based in Chicago. 

The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, the goal of this analysis is to understand **how annual members and casual riders use Cyclistic bikes differently**. Based on these insights, the marketing team will design strategies to convert casual riders into profitable annual members.

---

## 🏢 About the Company
In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of **5,824 bicycles** that are geotracked and locked into a network of **692 stations** across Chicago. 

Cyclistic offers flexible pricing options:
* **Casual Riders:** Customers who purchase single-ride or full-day passes.
* **Annual Members:** Customers who purchase an annual subscription.

Financial analysts have concluded that annual members are much more profitable than casual riders, making their conversion the primary target for future business growth.

---

## ⚙️ Data Analysis Process Phases

The project follows the six core phases of the data analysis process:

### 1. Ask
* **Business Task:** Design marketing strategies aimed at converting casual riders into annual members by identifying key behavioral differences between them.
* **Core Question:** How do annual members and casual riders use Cyclistic bikes differently?

### 2. Prepare
* **Data Source:** Historical bike trip data from Cyclistic (provided by Motivate International Inc. under an open data license). 
* **Data Structure:** Structured tabular data stored across 12 monthly CSV files representing a full year of bike trips.
* **Key Attributes:** `ride_id`, `rideable_type` (classic, electric, docked), `started_at`, `ended_at`, station names/IDs, location coordinates, and `member_casual` user flags.

### 3. Process
Data cleaning and transformation were completed to ensure data integrity and accuracy before analysis:
* **Duplicate Removal:** Identified and eliminated duplicate entries based on `ride_id`.
* **Validation:** Verified categorical columns like `rideable_type` and `member_casual` to filter out anomalies.
* **Data Consistency:** Trimmed whitespace and handled missing values across critical station location fields.
* **Feature Engineering:** * Created `ride_length` to calculate the exact duration of each ride (`ended_at` minus `started_at`).
    * Extracted `day_of_week`, `month`, and `hour` to analyze temporal usage patterns.
    * Removed negative or extreme outlier data where `started_at` occurred after `ended_at`.

### 4. Analyze & Share
Key findings uncovered during the exploratory data analysis (EDA):
* **Rider Breakdown:** Annual members consistently account for the majority of overall trips (~59%), while casual riders make up the remaining ~41%.
* **Ride Lengths:** Casual riders have significantly longer average ride durations (often double that of members), indicating leisure or recreational use.
* **Weekly Trends:** Annual members exhibit high, consistent usage from Monday through Friday (peaking during traditional commute hours at 8 AM and 5 PM). In contrast, casual riders show massive spikes on weekends (Saturdays and Sundays).
* **Seasonal Variations:** Overall bike usage peaks in the summer and drops heavily in the winter, but annual members maintain steadier utilization rates during the colder months compared to casual riders.

### 5. Act (Strategic Recommendations)
Based on the data insights, here are the top marketing strategies suggested to convert casual riders:
1.  **Weekend and Seasonal Memberships:** Introduce a specialized "Weekend-Only Pass" or a "Summer Membership" targeting casual riders who predominantly use the fleet for leisure during these peak periods.
2.  **Targeted Digital Marketing:** Deploy digital media ads focused at the top 10 starting and ending stations where casual rider traffic is heavily concentrated.
3.  **Financial Incentive & Loyalty Program:** Run targeted promotional campaigns demonstrating the cost-efficiency of an annual membership compared to recurring single/full-day pass purchases for heavy weekend users.

---

## 🛠️ Tools Used
* **Microsoft Excel:** Used for initial data assessment, schema verification, and quick sorting/filtering.
* **Tableau:** Employed to build interactive visual dashboards, line charts, and bar graphs to compare user group behaviors side-by-side.

Tableau dashboard link: https://public.tableau.com/views/Cyclistic_Case_Study_17746547636700/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

## 📸 Project Snapshots

### Dashboard
[![Cyclistic Dashboard](Screenshot%202026-11-06%20013834.png)](https://public.tableau.com/views/Cyclistic_Case_Study_17746547636700/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

### Key Insights & Recommendations
![Cyclistic Key Insights](Screenshot%202026-11-06%20013856.png)
