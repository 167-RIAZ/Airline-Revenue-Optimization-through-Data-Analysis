
# ✈️ Airline Revenue Optimization – Data Analysis Project

A comprehensive exploratory data analysis (EDA) project to help airlines optimize profitability by evaluating occupancy rates, ticket pricing, and aircraft performance using real-world booking and flight data.

---

## 🧠 Problem Statement

Airlines face challenges such as:
- Stricter environmental regulations
- Rising fuel prices and flight taxes
- High labor costs and competitive labor markets

**Goal:** Identify data-driven strategies to improve profitability, focusing on occupancy rate improvements and pricing optimizations.

---

## 🎯 Project Objectives

1. **Analyze aircraft seat utilization and ticket booking patterns**
2. **Evaluate fare condition pricing** (Economy, Business, Comfort)
3. **Assess revenue and occupancy metrics** for different aircraft models
4. **Simulate a 10% increase in occupancy rate** and estimate revenue impact
5. **Provide actionable recommendations** for pricing and operational strategies

---

## 📦 Dataset Overview

Data extracted from SQLite (`travel.sqlite`). Key tables:

| Table Name         | Description                                  |
|--------------------|----------------------------------------------|
| aircrafts_data     | Info about aircraft types and range          |
| airports_data      | Metadata of airports with coordinates        |
| bookings           | Customer booking records                     |
| boarding_passes    | Boarding details with seat allocation        |
| flights            | Flight schedules and aircrafts used          |
| seats              | Seat layout and fare categories per aircraft |
| ticket_flights     | Fare conditions and ticket price per flight  |
| tickets            | Passenger and booking reference details      |

---

## 🧪 Tools & Technologies

| Category         | Tools Used                |
|------------------|--------------------------|
| Language         | Python                    |
| Database         | SQLite3                   |
| Data Handling    | Pandas                    |
| Visualization    | Matplotlib, Seaborn       |
| IDE              | Jupyter Notebook          |

---

## 📊 Key Analyses & Visualizations

#### 1. Aircraft Seating Capacity  
Identify aircraft with >100 seats using SQL aggregation.

```sql
SELECT aircraft_code, COUNT(*) AS num_seats
FROM seats
GROUP BY aircraft_code
HAVING num_seats > 100;
```

#### 2. Ticket Booking and Revenue Trends  
- 📅 Tracked booking spikes and patterns
- 💰 Found correlation between ticket volume and revenue

#### 3. Fare Class Analysis  
- Business fares consistently higher than Economy
- Comfort class exclusive to aircraft 773
- CN1 & CR2 aircrafts offer only Economy fares

#### 4. Occupancy Rate Calculation  
- Formula: `occupancy_rate = booked_seats / total_seats`
- Simulated 10% increase in occupancy and its impact

#### 5. Revenue Simulation  
- Estimated revenue increase if all aircraft improved occupancy by 10%

#### 📈 Sample Visualizations
- Daily Ticket Sales (`assets/ticket_trend.png`)
- Average Fare by Fare Condition (`assets/fare_conditions.png`)
- Occupancy Rate Per Aircraft (`assets/occupancy_rate.png`)

---

## 📚 Key Insights

- ✈️ Aircraft SU9 generated highest revenue due to high volume and occupancy, despite lower ticket prices
- ❌ Aircraft CN1 had lowest revenue due to fewer seats and only Economy fare
- 📈 10% occupancy increase = significant annual turnover rise
- 💡 Price adjustments and aircraft-specific fare restructuring needed

---

## 💡 Recommendations

- 🎯 Focus on underperforming aircraft (e.g., CN1, CR2); analyze routes and service quality
- 🪙 Use dynamic pricing during high-demand periods
- 🚀 Expand popular fare types (e.g., Comfort) to more aircraft
- 📆 Leverage seasonal booking patterns for optimized scheduling

---

## 🗂️ Project Structure

```
📁 Airline-Revenue-Analysis
├── 📄 Airlines Data Analysis.ipynb
├── 📄 Report.pdf
├── 📄 travel.sqlite
├── 📁 assets/
│   ├── ticket_trend.png
│   ├── fare_conditions.png
│   └── occupancy_rate.png
└── 📄 README.md
```

---

## 🚀 Getting Started

1. Clone the repository  
   `git clone https://github.com/167-RIAZ/Airline-Revenue-Optimization-through-Data-Analysis.git`
2. Install Python dependencies  
   `pip install pandas matplotlib seaborn`
3. Open `Airlines Data Analysis.ipynb` in Jupyter Notebook
4. Make sure `travel.sqlite` is present in the root folder

---

## 🙋‍♂️ About Me

Syed Md Riaz  
Passionate about solving business problems with data  
📧 syed.riaz1406@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/syedmdriaz)

---

## 📄 License

Open for academic, learning, and portfolio use only.

---

## 🔗 Let’s Connect!

If you found this project helpful or have suggestions, feel free to reach out or fork the repo. Collaboration is always welcome!
