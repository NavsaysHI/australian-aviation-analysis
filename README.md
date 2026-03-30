# Australian Domestic Aviation Performance Analysis (2010–2026)

End-to-end data analytics project analyzing 16 years of Australian domestic aviation data using official BITRE sources.

## 🔗 Live Dashboard
**[View Interactive Tableau Dashboard](https://public.tableau.com/views/AustralianDomesticAviationPerformanceAnalysis/Dashboard1)**

## 📊 Project Overview

This project analyzes Australian domestic aviation performance from 2010–2026, covering:
- **24,000+** route-month records across 100+ routes
- **13,540** fare observations 
- **520** airline on-time performance records
- COVID-19 impact and recovery patterns

### Key Insights
- **MEL-SYD** (Melbourne-Sydney) is the dominant route with 8.1M passengers annually (2025)
- Average real airfares dropped 14% during COVID (2021) before recovering to near pre-pandemic levels
- Domestic passenger volume collapsed 65% in 2020, recovered to 96% of 2019 levels by 2025
- Major routes show differentiated recovery patterns post-COVID

## 🛠️ Tech Stack

- **Excel**: Data cleaning, validation, transformation
- **SQLite**: Relational database design, data modeling
- **SQL**: Analytical queries for business insights
- **Tableau**: Interactive data visualization and dashboards

## 📁 Project Structure
```
├── australian_aviation_analysis.db    # SQLite database (4 tables)
├── route_performance_monthly.csv      # 8,239 route-month records (2014-2025)
├── air_fares_monthly.csv              # 13,540 fare observations (2010-2026)
├── on_time_performance_2024_25.csv    # 520 airline-route OTP records
├── annual_summary_june_2025.csv       # 62 top routes annual summary
├── top_20_routes_2025.csv             # SQL query output
├── fare_trends_by_year.csv            # SQL query output
├── monthly_passenger_trends.csv       # SQL query output
├── airline_otp_rankings_2024_25.csv   # SQL query output
└── major_routes_growth_analysis.csv   # SQL query output
```

## 📈 Data Pipeline

### 1. Data Collection
- Source: [BITRE (Bureau of Infrastructure and Transport Research Economics)](https://www.bitre.gov.au/statistics/aviation)
- 4 official datasets covering routes, fares, on-time performance, and annual summaries

### 2. Data Cleaning (Excel)
- Removed COVID-period data gaps (2020-2021 confidentiality restrictions)
- Created route identifiers from airport codes (e.g., "MEL-SYD")
- Validated data integrity across 8,239 route-month records
- Standardized column names and data types

### 3. Database Design (SQLite)
```sql
-- 4 normalized tables:
routes           -- Route performance metrics (8,239 records)
fares            -- Monthly fare trends (13,540 records)
otp              -- On-time performance by airline (520 records)
summary          -- Annual route summaries (62 records)
```

### 4. SQL Analysis
Key analytical queries:
- Top 20 routes by passenger volume (2025)
- Fare trends over 16 years (2010-2026)
- Monthly passenger time series showing COVID impact
- Airline on-time performance rankings
- Major routes growth analysis (6 trunk routes)

### 5. Visualization (Tableau)
Interactive dashboard with 4 views:
1. **Route Rankings**: Top 20 routes by passenger volume
2. **Fare Trends**: Real airfare movements (inflation-adjusted)
3. **COVID Impact**: Monthly passenger volume showing 2020 collapse and recovery
4. **Route Growth**: Multi-line comparison of major trunk routes

## 🎯 Business Context

**Target Application**: Data Analyst roles in aviation industry (Virgin Australia, Qantas, regional airlines)

**Demonstrates**:
- Understanding of aviation KPIs (Load Factor, RPK/ASK, OTP)
- Ability to source and work with government statistical data
- Full-stack data analytics capability (collection → cleaning → analysis → visualization)
- Business insight generation from complex datasets

## 📊 Key Metrics Analyzed

- **Revenue Passengers**: Total paying passengers carried
- **Load Factor (PLF)**: Seat utilization percentage (Revenue Pax ÷ Available Seats × 100)
- **RPK (Revenue Passenger Kilometres)**: Passengers × distance flown
- **ASK (Available Seat Kilometres)**: Capacity metric (total seats × distance)
- **On-Time Performance**: % of flights arriving within 15 minutes of schedule
- **Real Fares**: CPI-adjusted to 2026 dollars for inflation comparison

## 📝 Methodology Notes

- **Data Quality**: Removed 700+ records with "Data not available for release" (COVID confidentiality)
- **Time Period**: Primary analysis 2014-2025 (routes), extended to 2010-2026 (fares)
- **Scope**: Domestic Regular Public Transport (RPT) operations only, excludes charter
- **Route Definition**: City pairs in both directions (bidirectional)

## 👤 Author

**Navdeep Rao**  
Data Analyst | Brisbane, Australia  
[LinkedIn](https://linkedin.com/in/navdeep-rao-58504311a) | [GitHub](https://github.com/NavsaysHI)

---

*Data Source: Bureau of Infrastructure and Transport Research Economics (BITRE)*  
*Project Type: Portfolio / Self-Directed Learning*
