# 🏏 ICC Men's T20 World Cup 2022 – Best XI (Data Analytics Project)

This is a personal data analytics project where I analyzed player performance from the ICC Men's T20 World Cup 2022 to build an optimal Best XI team. The project focuses on key metrics like strike rate, batting average, boundary percentage, and economy rate, and presents the results using Power BI.

---

## 📌 Project Objective

To analyze complete tournament data from the ICC Men's T20 World Cup 2022 (including Qualifier and Super 12 stages) and select a statistically strong playing XI using key performance metrics.

---

## ⚙️ Tools Used

- **Power BI** – For data cleaning, transformation (Power Query), and visual analysis
- **Jupyter Notebook (Python)** – For initial data checks and exploration
- **Excel** – Used for metric logic testing and quick review

---

## 🧠 Methodology

- **Data Source**: Stats were taken from ESPN Cricinfo (pre-scraped data was used to focus on analysis)
- **Cleaning**: Performed using Power BI Load & Transform (removed extra columns, fixed formats, and handled missing values)
- **Filtering**: Players with very low match participation were excluded to maintain quality
- **Role Classification**: Based on strike rate, boundary %, average, and bowling economy
- **Best XI Selection**: Chosen by comparing players within roles (openers, middle order, finishers, bowlers, all-rounders)

---

## 📊 Key Metrics Used

- **Batting Average** – Consistency of scoring
- **Strike Rate** – Scoring speed
- **Boundary Percentage** – Aggressive impact
- **Dot Ball Percentage** – Pressure created by bowlers
- **Economy Rate** – Efficiency in conceding runs
- **Bowling Average & Strike Rate** – Effectiveness in taking wickets

---

## 📐 DAX Measures Used in Power BI
| **Metric**          | **DAX Formula**                                                                             | **Table**              | **Purpose**                                    |
| ------------------- | ------------------------------------------------------------------------------------------- | ---------------------- | ---------------------------------------------- |
| Total Runs          | `Total Runs = SUM(fact_batting_summary[runs])`                                              | fact\_batting\_summary | Total runs scored by a batsman                 |
| Batting Average     | `Batting Avg = DIVIDE([Total Runs],[Total Innings Dismissed],0)`                            | fact\_batting\_summary | Measures scoring consistency                   |
| Strike Rate         | `Strike rate = DIVIDE([Total Runs],[total balls faced],0)*100`                              | fact\_batting\_summary | Indicates scoring speed                        |
| Boundary Percentage | `Boundary % = DIVIDE(SUM(fact_batting_summary[Boundary runs]), [Total Runs], 0)`            | fact\_batting\_summary | Measures aggressive impact                     |
| Dot Ball Percentage | `Dot ball % = DIVIDE(SUM(fact_bowling_summary[zeros]), SUM(fact_bowling_summary[balls]),0)` | fact\_bowling\_summary | Measures pressure created by bowlers           |
| Economy Rate        | `Economy = DIVIDE([Runs Conceded], ([balls Bowled]/6), 0)`                                  | fact\_bowling\_summary | Runs conceded per over                         |
| Bowling Average     | `Bowling Average = DIVIDE([Runs Conceded], [wickets], 0)`                                   | fact\_bowling\_summary | Runs conceded per wicket taken                 |
| Bowling Strike Rate | `Bowling Strike Rate = DIVIDE([balls Bowled], [wickets], 0)`                                | fact\_bowling\_summary | Balls per wicket                               |

---

## 🔗 Connect With Me

📧 jkmevada.2003@gmail.com  
🔗 [LinkedIn – jkmevada](https://linkedin.com/in/jkmevada)

---

## 📂 Note

This project was made for portfolio and learning purposes. All stats are taken from publicly available sources and transformed for educational use.
