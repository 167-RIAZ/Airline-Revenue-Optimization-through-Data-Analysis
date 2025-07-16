

# ✈️ Airlines Revenue Optimization – Data Analysis Project

A comprehensive exploratory data analysis (EDA) project designed to help an airline optimize its profitability by evaluating occupancy rates, ticket pricing, and aircraft performance using real-world airline booking data.

---

## 🧠 Problem Statement

Due to challenges such as:
- Stricter environmental regulations
- Rising fuel prices and flight taxes
- High labor costs and tight labor markets

the airline is seeking **data-driven strategies** to improve profitability. The main goal is to identify how **occupancy rate improvements and pricing optimizations** can positively impact total revenue.

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

