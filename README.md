# AI-Powered Fleet Performance & Delivery Efficiency Dashboard  

The objective is to analyze fleet performance for a logistics company by evaluating
delivery efficiency, fuel usage, and operational cost using Power BI and AI visuals.

This repository focuses on **conceptual explanation**, not implementation or DAX formulas.

---

## Business Scenario

A logistics company wants to improve operational efficiency by analyzing:
- On-time delivery performance
- Fuel efficiency of vehicles
- Cost per kilometer
- Vehicle maintenance impact

The dashboard is designed to support **route optimization, fleet utilization, and cost control**.

---

## Dataset Overview

The analysis is based on a single Excel file:

### `logistics_project_dataset.xlsx`

#### 1. Trip_Data Table
Contains trip-level operational data:
- Trip ID
- Vehicle ID
- Driver ID
- Origin and Destination
- Distance traveled (km)
- Fuel consumed (liters)
- Delivery status (On-Time / Late)
- Delivery date

This table represents **day-to-day logistics operations**.

---

#### 2. Vehicle_Master Table
Contains vehicle-level reference data:
- Vehicle ID
- Vehicle type
- Capacity
- Maintenance cost

This table provides **contextual attributes** required for cost and efficiency analysis.

---

## Data Cleaning & Data Modeling (Conceptual)

### Missing Fuel Consumption Handling
Some trips contain missing fuel consumption values.

Approach:
- Replace missing values using **mean imputation**

Purpose:
- Ensures fuel efficiency calculations are not distorted
- Prevents broken measures and misleading visuals

---

### Data Relationships
A relationship is created between:
- `Trip_Data[Vehicle_ID]`
- `Vehicle_Master[Vehicle_ID]`

Purpose:
- Enables vehicle-level cost and type analysis
- Allows combined insights across operational and master data

Without this relationship, cost and efficiency analysis is invalid.

---

## Key Metrics (Business Meaning)

### Fuel Efficiency
Represents how efficiently fuel is converted into distance traveled.

Why it matters:
- Identifies inefficient vehicles or driving behavior
- Supports fuel optimization strategies

---

### On-Time Delivery Percentage
Measures reliability of deliveries.

Why it matters:
- Directly impacts customer satisfaction
- Helps identify problematic destinations or routes

---

### Cost per Kilometer
Represents operational cost normalized by distance.

Cost components include:
- Fuel cost (fixed assumption)
- Vehicle maintenance cost

Why it matters:
- Allows fair comparison across trips and vehicles
- Highlights expensive routes or vehicle types

---

## Visual Analysis (Purpose of Each Visual)

### Bar Chart – On-Time Delivery % by Destination
Shows delivery performance across destinations.

Business value:
- Identifies regions with frequent delays
- Supports route and scheduling improvements

---

### Line Chart – Fuel Efficiency Trend by Delivery Date
Displays changes in fuel efficiency over time.

Business value:
- Detects performance degradation
- Helps monitor vehicle health and driver behavior

---

### KPI Cards

#### Average Delivery Time
Provides a quick view of delivery speed.

#### Average Cost per Kilometer
Summarizes operational cost efficiency.

Business value:
- Enables executive-level monitoring
- Supports quick decision-making

---

### Pie Chart – Vehicle Type vs Average Maintenance Cost
Shows maintenance cost distribution by vehicle type.

Business value:
- Identifies high-maintenance vehicle categories
- Supports fleet replacement decisions

---

## AI-Powered Visuals (Conceptual Use)

### Q&A Visual
Allows natural language questions such as:
- “Average cost per km by vehicle type?”

Business value:
- Enables self-service analytics
- Reduces dependency on manual reports

---

### Key Influencers Visual
Analyzes what factors influence delivery status.

Explained by:
- Distance traveled
- Vehicle type
- Driver ID

Business value:
- Identifies root causes of late deliveries
- Supports targeted interventions

---

### Decomposition Tree
Breaks down cost per kilometer into contributing factors:
- Vehicle type
- Maintenance cost
- Distance traveled

Business value:
- Enables deep cost diagnostics
- Helps decision-makers explore cost drivers interactively

---

## Expected Outcome

The final dashboard enables:
- Optimization of delivery routes
- Better fleet utilization
- Cost reduction through data-driven decisions
- Improved on-time delivery performance

This project demonstrates **end-to-end Power BI capability**, combining
data modeling, business metrics, visual analytics, and AI-powered insights.

---

## Key Takeaways

- Data quality directly impacts insight quality
- Relationships are the backbone of Power BI analysis
- AI visuals enhance exploration, not replace thinking
- Dashboards must answer business questions, not just display data
