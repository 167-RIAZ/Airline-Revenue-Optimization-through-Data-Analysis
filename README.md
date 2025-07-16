
# ✈️ Airlines Revenue Optimization – Data Analysis Project

A comprehensive exploratory data analysis (EDA) project designed to help an airline optimize its profitability by evaluating occupancy rates, ticket pricing, and aircraft performance using real-world airline booking data.

---

## 🧠 Problem Statement

Due to challenges such as:
- Stricter environmental regulations
- Rising fuel prices and flight taxes
- High labor costs and tight labor markets

The airline is seeking **data-driven strategies** to improve profitability. The main goal is to identify how **occupancy rate improvements and pricing optimizations** can positively impact total revenue.

---

## 🎯 Project Objectives

1. **Analyze aircraft seat utilization** and ticket booking patterns.  
2. **Evaluate fare condition pricing** (Economy, Business, Comfort).  
3. **Assess revenue and occupancy metrics** for different aircraft models.  
4. **Simulate a 10% increase in occupancy rate** and estimate the revenue impact.  
5. Provide **data-backed recommendations** for pricing and operational strategies.  

---

## 📦 Dataset Overview

Data was extracted from a SQLite relational database (`travel.sqlite`) and included the following tables:

| Table Name         | Description                                  |
|--------------------|----------------------------------------------|
| `aircrafts_data`   | Info about aircraft types and range          |
| `airports_data`    | Metadata of airports including coordinates   |
| `bookings`         | Records of customer bookings                 |
| `boarding_passes`  | Boarding details with seat allocation        |
| `flights`          | Flight schedule and aircraft used            |
| `seats`            | Seat layout and fare categories per aircraft |
| `ticket_flights`   | Fare conditions and ticket price per flight  |
| `tickets`          | Passenger and booking reference details      |

---

## 🧪 Tools & Technologies

| Category        | Tools Used                  |
|----------------|-----------------------------|
| Language        | Python                      |
| Database        | SQLite3                     |
| Data Handling   | Pandas                      |
| Visualization   | Matplotlib, Seaborn         |
| IDE             | Jupyter Notebook            |

---

## 📊 Key Analyses & Visualizations

### ✅ 1. Aircraft Seating Capacity  
Identified aircraft with more than 100 seats using SQL aggregation:

```sql
SELECT aircraft_code, COUNT(*) AS num_seats
FROM seats
GROUP BY aircraft_code
HAVING num_seats > 100;


⸻

 ✅ 2. Ticket Booking and Revenue Trends

Tracked how bookings and revenue changed over time using line plots:
	•	🗓️ Ticket volume peaks: Identified booking spikes.
	•	💰 Revenue correlation: Revenue patterns matched ticket volume trends.

⸻

✅ 3. Fare Class Analysis

Compared average fare per aircraft and fare class:
	•	Business fares were consistently higher than Economy.
	•	Comfort class was available only in aircraft 773.
	•	Aircrafts CN1 and CR2 offered only Economy fares.

⸻

✅ 4. Occupancy Rate Calculation

Calculated average seat occupancy per aircraft:

occupancy_rate = booked_seats / total_seats

Simulated the impact of a 10% increase in occupancy.

⸻

✅ 5. Revenue Simulation

Estimated potential revenue increase if all aircraft improved occupancy by 10%.

⸻

📈 Sample Visualizations
	•	🎟️ Daily Ticket Sales
	•	🛫 Average Fare by Fare Condition
	•	📉 Occupancy Rate Per Aircraft

(Visuals are created using Seaborn and Matplotlib. See assets/ folder.)

⸻

📚 Key Insights
	•	✈️ Aircraft SU9 generated the highest total revenue despite lower ticket prices—thanks to high volume and occupancy.
	•	❌ Aircraft CN1 had the lowest revenue likely due to fewer seats and only offering Economy fare.
	•	📈 A 10% increase in average occupancy showed a significant rise in annual turnover.
	•	💡 Price adjustments and aircraft-specific fare restructuring are needed for profit maximization.

⸻

💡 Recommendations
	•	🎯 Focus on underperforming aircraft (e.g., CN1, CR2) and analyze routes or service quality.
	•	🪙 Implement dynamic pricing to maximize revenue during high-demand periods.
	•	🚀 Expand popular fare types (e.g., Comfort) to additional aircrafts.
	•	📆 Analyze seasonal booking patterns for more strategic scheduling.

⸻

🗂️ Project Structure

📁 Airlines-Revenue-Analysis
├── 📄 Airlines Data Analysis.ipynb
├── 📄 Report.pdf
├── 📄 travel.sqlite
├── 📁 assets/
│   ├── ticket_trend.png
│   ├── fare_conditions.png
│   └── occupancy_rate.png
└── 📄 README.md


⸻

🙋‍♂️ About Me

Syed Md Riaz
Passionate about solving business problems using data
📧 syed.riaz1406@gmail.com
🔗 [LinkedIn]->https://linkedin.com/in/syedmdriaz


⸻

📄 License

This project is open for academic, learning, and portfolio use only.

⸻

🔗 Let’s Connect!

If you found this project helpful or have suggestions, feel free to reach out or fork the repo.
Collaboration is always welcome!

