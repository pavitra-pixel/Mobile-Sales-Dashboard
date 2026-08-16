# 📱Mobile Sales Performance Dashboard
An interactive, single-page Power BI report analyzing three years of mobile phone retail transactions across India — tracking sales, brand and model performance, city-level demand, and customer satisfaction in one filterable view.

## Short Description / Purpose
The Mobile Sales Dashboard is a Power BI report designed to help retail sales managers, category analysts, and business teams understand how mobile phone sales performed across 19 Indian cities between late 2021 and late 2024. It tracks core sales KPIs (revenue, quantity, average price, transactions), visualizes monthly demand trends and weekday patterns, compares performance across 5 brands and 15 models, maps revenue concentration by city, and breaks down customer satisfaction and payment method preference — all filterable by month, brand, model, and payment method via interactive slicers.

## Tech Stack
The dashboard was built using the following tools and technologies:
- 📊 Power BI Desktop – Main data visualization platform used for report creation
- 📁 Power Query – Data cleaning and transformation layer (standardizing inconsistent day-name entries, shaping the transaction table for modeling)
- 🧮 DAX (Data Analysis Expressions) – Used for calculated KPI measures (Total_sales, Total_quantity, Average_price, Transactions) and a calculated Rating Status column bucketing 1–5 star ratings into Poor/Average/Good/Excellent
- 📄 Data Modeling – Mobile_Sales_Data fact table joined to a custom date table (Custom_Calander) for month-level time intelligence, enabling cross-filtering across all visuals via slicers
- 📁 File Format – .pbix for development, .xlsx as the raw data source, .png for dashboard previews

## Data Source
Source: Mobile_Sales_Data.xlsx — a transaction-level mobile phone sales dataset.

Contains 3,835 transaction records spanning October 2021 – October 2024, across 19 Indian cities, 5 brands (Apple, Samsung, OnePlus, Vivo, Xiaomi), and 15 mobile models. Each row represents one transaction, with fields for transaction ID, day/month/year/day name, brand, mobile model, units sold, price per unit, customer name, customer age (18–59), city, payment method, and customer rating (1–5 stars).

## Features / Highlights
- **Business Problem:** Mobile retailers generate thousands of transactions across brands, models, cities, and payment channels but often lack an easy way to see which brands and models are actually winning, where regional demand concentrates, how satisfied customers are, and which payment methods dominate — making it hard to guide inventory, city-level expansion, and marketing spend.
  
- **Goal of the Dashboard:** To deliver an interactive visual tool that:
  
  - Tracks headline sales KPIs at a glance, filterable by month, brand, model, and payment method
  - Reveals monthly and weekday demand patterns to support seasonal planning
  - Segments customer satisfaction into clear rating tiers
  - Compares brand and model performance side-by-side
  - Visualizes geographic revenue concentration through a city-level map
  - Breaks down payment method preference across the customer base
    
- **Walkthrough of Key Visuals**
  
  - KPI Cards (Top): Total Sales ₹76.92 Cr (₹769,204,987.97) · Total Quantity 19,150 units · Average Price ₹40,114 · Transactions 3,835
  - Slicers: Month, Mobile Model, Payment Method, and Brand — filter every visual on the page interactively
  - Monthly Trend (Line Chart): Units sold by month — July peaks at 1,700 units, February is lowest at 1,451, showing a mild mid-year demand lift
  - Rating Status (Funnel): Ratings bucketed into Excellent/Good/Average/Poor — Excellent-rated purchases lead by a wide margin, and 60.8% of all transactions (2,331 of 3,835) are rated 4 or 5 stars
  - Payment Method (Donut): Transaction share is nearly even — UPI (26.4%), Debit Card (24.7%), Credit Card (24.7%), Cash (24.2%) — with UPI holding a slight lead
  - Sales by Mobile Model (Clustered Bar): iPhone SE tops at ₹5.96 Cr, Redmi 9 lowest at ₹4.47 Cr — a tight spread across all 15 models
  - Sales by Day Name (Area Chart): Saturday is the strongest sales day (₹11.46 Cr), Wednesday the weakest (₹10.49 Cr) — demand stays fairly flat across the week
  - Sales by City (Map): Delhi leads at ₹20.39 Cr (26.5% of revenue), Mumbai second at ₹12.72 Cr (16.5%) — together the top 2 of 19 cities drive 43% of total sales
  - Brand Summary (Table): Apple leads narrowly at ₹16.16 Cr / 783 transactions / 3,932 units, closely followed by Samsung, OnePlus, Vivo, and Xiaomi — all five brands sit within ₹1.8 Cr of each other

- **Business Impact & Insights**

  - Regional Investment: Delhi and Mumbai alone drive 43% of revenue — strong candidates for dedicated inventory and localized marketing spend, while the remaining 17 cities each hold a smaller, fairly even share, pointing to expansion headroom
  - Brand Portfolio Balance: No single brand dominates (Apple leads Samsung by under 1%) — the retailer's assortment is well-diversified, so decisions are better made at the model level than the brand level
  - Customer Satisfaction: With 60.8% of transactions rated 4–5 stars against just 22.2% rated 1–2 stars, overall satisfaction is healthy, though the ~22% negative-rated segment is worth investigating for common causes
  - Digital Payment Readiness: UPI and card payments together make up over 75% of transactions — checkout and POS systems should prioritize digital flows, while cash (24%) still needs reliable support
  - Seasonal Demand: The July uptick in units sold (1,700 vs. 1,451 in February) suggests a seasonal window worth planning promotions and inventory around

## Screenshots / Demos
![Dashboard](https://github.com/pavitra-pixel/mobile-sales-dashboard/blob/main/Mobile%20Sales%20Dashboard.png)
