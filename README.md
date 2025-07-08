# 🏏 ICC Men's T20 World Cup 2022 – Best XI (Data Analytics Project)

This is a self-driven data analytics project where I analyzed player performance from the ICC Men's T20 World Cup 2022 to build an optimal **Best XI team**.  
The focus was on key metrics like **strike rate**, **batting average**, **boundary percentage**, and **economy rate**, and the results are visualized using an interactive Power BI dashboard.

---

## 📊 Live Dashboard Preview

![Dashboard Screenshot](images/t20_dashboard_preview.png)

🔗 **[Click here to explore the live Power BI dashboard](https://app.powerbi.com/view?r=eyJrIjoiOGFkMDU1MTgtNjg0Zi00MjU3LTkyYWEtMzU3ZDE2Mjc2NzQ3IiwidCI6IjVhMGZhNzk3LTgzNjgtNDY5Ni05MTBjLWZjODdhYzQ2NjlmZiJ9&pageName=ReportSection3a8cb23b814911c94608)**  
*(Best viewed on desktop or full-screen mode)*

---

## 📌 Project Objective

To analyze full tournament data from the **ICC Men's T20 World Cup 2022** — including **Qualifier** and **Super 12** stages — and select a performance-based **Best XI** using meaningful KPIs.

---

## ⚙️ Tools Used

- **Power BI** – For data transformation, modeling, and dashboard design  
- **Jupyter Notebook (Python)** – For initial JSON processing and cleanup  
---

## 🧠 Methodology

- **Data Source**: Player stats were taken from **ESPN Cricinfo** (scraped and shared as JSON files)
- **Cleaning & Transformation**: Handled in Jupyter (Python) and Power BI (Power Query)
- **Filtering**: Players with very low match participation were excluded to ensure meaningful comparisons
- **Role Classification**: Based on strike rate, boundary %, average, and bowling economy
- **Final XI Selection**: Players were picked within their role groups ( openers, anchors, finishers, all-rounders, and specialist bowlers ) based on overall contribution and consistency

---

## 📊 Key Metrics Used

| Category | Metrics |
|----------|---------|
| **Batting** | Batting Average, Strike Rate, Boundary Percentage |
| **Bowling** | Economy Rate, Dot Ball %, Bowling Average, Bowling Strike Rate |

---

## 📐 DAX Measures Used in Power BI

| **Metric**            | **DAX Formula**                                                                                  | **Table**               | **Purpose**                                        |
|----------------------|--------------------------------------------------------------------------------------------------|-------------------------|----------------------------------------------------|
| Total Runs            | `Total Runs = SUM(fact_batting_summary[runs])`                                                  | `fact_batting_summary`  | Total number of runs scored                        |
| Batting Average       | `Batting Avg = DIVIDE([Total Runs], [Total Innings Dismissed], 0)`                              | `fact_batting_summary`  | Measures batting consistency                       |
| Strike Rate           | `Strike Rate = DIVIDE([Total Runs], [Total Balls Faced], 0) * 100`                              | `fact_batting_summary`  | Measures scoring speed                             |
| Boundary Percentage   | `Boundary % = DIVIDE(SUM(fact_batting_summary[Boundary runs]), [Total Runs], 0)`                | `fact_batting_summary`  | Indicates aggressive intent                        |
| Dot Ball Percentage   | `Dot Ball % = DIVIDE(SUM(fact_bowling_summary[zeros]), SUM(fact_bowling_summary[balls]), 0)`    | `fact_bowling_summary`  | Measures bowling pressure                          |
| Economy Rate          | `Economy = DIVIDE([Runs Conceded], ([Balls Bowled] / 6), 0)`                                    | `fact_bowling_summary`  | Runs conceded per over                             |
| Bowling Average       | `Bowling Average = DIVIDE([Runs Conceded], [Wickets], 0)`                                       | `fact_bowling_summary`  | Runs conceded per wicket                           |
| Bowling Strike Rate   | `Bowling Strike Rate = DIVIDE([Balls Bowled], [Wickets], 0)`                                    | `fact_bowling_summary`  | Balls taken to get a wicket                        |

---
## 📷 Project Deliverables

- 📓 **Python notebook** to preprocess and clean JSON files into structured CSVs  
- 📊 **Power BI dashboard** with filters, interactivity, and key metric visualizations  
- 🎯 **Presentation** summarizing logic, methodology, insights, and the final team  
- 📄 [View Full Presentation (PDF)](documents/WC_T20_2022_Best_11-Presentation.pdf)


---

## 🔗 Connect With Me

📧 jkmevada.2003@gmail.com  
🔗 [LinkedIn – jkmevada](https://linkedin.com/in/jkmevada)

---

## 🧾 Additional Info

- The datasets used were publicly available and processed using a full analytics pipeline — from raw JSON to a published Power BI dashboard.
- This project reflects my ability to handle end-to-end data analytics: **data cleaning, metric design, DAX logic, and visual storytelling**.
- The approach mirrors what’s expected in real-world sports or business analytics scenarios.
