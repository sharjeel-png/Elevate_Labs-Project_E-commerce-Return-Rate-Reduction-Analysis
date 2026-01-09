# 📦 Elevate Labs Project E-commerce Return Rate Reduction Analysis

## 📌 Project Overview
This project analyzes historical e-commerce order and return data and builds a predictive return risk model to identify products that are more likely to be returned in the future.  
The solution combines Python (for machine learning) and Power BI (for interactive dashboards) to deliver both descriptive and predictive business insights.

---

## 🎯 Objectives
- Provide a high-level e-commerce performance summary
- Understand why customers return products
- Analyze return behavior by category, market, product, and region
- Predict future return risk using machine learning
- Enable interactive exploration through dashboards and drill-through

---

## 🛠 Tools & Technologies
- Python: Data processing & Logistic Regression  
- Power BI: Interactive dashboards, drill-through, bookmarks  
- Excel / CSV: Source data and model output storage  

---

## 📂 Dataset Description
The project uses the Global Superstore dataset, which includes:
- Orders: All historical customer orders  
- Returns: Orders that were returned  
- People: Region-to-person mapping  

---

## 🧠 Methodology

### Data Preparation
- Orders and Returns were joined using Order ID
- A binary target variable Returned was created:
  - 1 → Order was returned  
  - 0 → Order was not returned  

### Predictive Modeling (Python)
- A Logistic Regression model was trained to predict the probability of return
- Features used:
  - Category
  - Sub-Category
  - Segment
  - Market
  - Ship Mode
  - Discount
  - Quantity
  - Sales
- Model output:
  - Return_Risk_Score (probability between 0 and 1)

### Risk Aggregation
- Order-level risk scores were aggregated at product level
- Products were classified into Low, Medium, and High Risk
- Final output exported as:
  high_risk_products.csv

---

## 📊 Power BI Dashboard Structure

### Page 1 – E-commerce Summary
- Total Orders
- Total Sales
- Total Returns
- Return Rate
- Key trends across time and markets  
Purpose: Provide executives a quick snapshot of overall e-commerce health.

### Page 2 – Returns Overview
- Total Returns
- Return Rate
- Return trends by Category, Market, and Time
- Cross-filtering between visuals  
Purpose: Understand what is being returned and where.

### Page 3 – Return Analysis
- Deeper analysis by Product, Category, Market, and Person (region-level)
- Interactive visuals with cross-filtering  
Purpose: Identify patterns and problem areas behind returns.

### Page 4 – Detailed View
- Drill-through target page
- Product-level and order-level details
- Reset Filters button implemented using bookmarks  
Purpose: Enable deep investigation of selected products or categories.

### Page 5 – Return Risk Dashboard
- Built using high_risk_products.csv
- Top products by predicted return risk
- Average risk by category
- Historical product metrics vs predicted risk  
Purpose: Highlight future-focused risk for proactive decision-making.

---

## 🔁 Interactivity Features
- Cross-filtering between visuals
- Slicers for dynamic exploration
- Drill-through from analysis pages to Detailed View
- Reset Filters button for improved user experience

---

## 📦 Deliverables Status

- Interactive dashboard with drill-through filters: ✅ Complete
- Python codebase for prediction: ✅ Complete
- CSV of high-risk products: ✅ Complete

---

## 🧾 Key Business Insight
Although overall return rates are low, relative differences in predicted return risk help identify products that require proactive quality, pricing, or logistics review.

---

## 🧠 Key Learning
For rare events like product returns, predictive models are most valuable for ranking and comparison, not absolute probabilities.

---

## 📌 One-Line Project Summary
An end-to-end e-commerce analytics project combining Python-based return risk prediction with Power BI dashboards to support proactive return reduction strategies.
