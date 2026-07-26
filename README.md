# 🚛 Logistics Operations Performance Dashboard (Microsoft Excel)

**An interactive Excel dashboard that transforms logistics operations data into executive-ready insights using Power Query, Power Pivot, DAX, and Pivot Tables.**

![Dashboard Preview](Images/Dashboard.png)

---

# 📖 Project Overview

Logistics organizations generate thousands of operational records every day, from trips and deliveries to maintenance, fuel consumption, and incidents. While this data is valuable, decision-makers often struggle to convert it into timely, actionable insights.

This project demonstrates how **Microsoft Excel** can be used as a Business Intelligence platform to consolidate operational data into an interactive dashboard that supports strategic decision-making.

The solution consists of three integrated components:

* **Fleet Operations Dashboard** – Executive KPIs and interactive visualizations
* **Executive Insight Page** – Business findings and recommendations
* **Operational Report Page** – Supporting tables for detailed analysis

---

# 🎯 Business Objective

Design an interactive dashboard that enables management to monitor:

* Fleet performance
* Financial performance
* Customer service
* Maintenance activities
* Safety incidents
* Facility workload
* Truck performance

while reducing reliance on manual reporting.

---

# ❓ Business Questions Answered

The dashboard was designed around real business questions rather than simply visualizing data.

### Financial Performance

* Is revenue consistently exceeding operating costs?
* Which periods experienced the weakest financial performance?

### Fleet Operations

* Is fleet utilization being optimized?
* Does downtime affect operational activity?

### Customer Service

* How reliable is our On-Time Delivery performance?
* Which customers generate the highest delivery demand?

### Maintenance

* Which maintenance categories consume the largest share of maintenance spending?

### Safety

* Which cities experience the highest operational risks?
* How severe are the recorded incidents?

### Facilities

* Which facilities process the largest operational workload?

### Asset Performance

* Which trucks perform best overall?
* Which assets require operational attention?

---

# 📊 Dashboard Features

## Executive KPIs

* Total Trips
* Total Revenue
* Operating Cost
* Fleet Utilization
* Fuel Efficiency
* On-Time Delivery Rate

---

## Interactive Filters

* Year
* Month
* Truck ID

---

## Visualizations

* Revenue vs Operating Cost
* Fleet Activity (Trips) vs Downtime
* Top Customers by Deliveries
* Top Facilities by Loads
* Maintenance by Type
* Incidents by City & Severity

---

## Supporting Analysis

The report page provides detailed operational tables including:

* Truck Performance Comparison
* Revenue vs Operating Cost
* Trips vs Downtime
* Customer Deliveries
* Facility Loads
* Incidents Severity

---

# 🛠 Technical Stack

| Tool            | Purpose                        |
| --------------- | ------------------------------ |
| Microsoft Excel | Dashboard Development          |
| Power Query     | Data Cleaning & Transformation |
| Power Pivot     | Data Modeling                  |
| DAX             | KPI Calculations               |
| Pivot Tables    | Aggregation                    |
| Pivot Charts    | Interactive Visualizations     |
| Slicers         | Dynamic Filtering              |

---

# 🗂 Data Model

The dashboard uses a relational data model built in **Power Pivot**.

![Data Model](Images/Data_Model.png)

### Fact Tables

* Trips
* Loads
* Deliveries
* Fleet Utilization
* Fuel Purchases
* Maintenance Records
* Incidents

### Dimension Tables

* Calendar
* Trucks
* Customers
* Facilities
* Drivers

---

# 🧹 Data Quality Assessment

Before analysis, the dataset was validated to improve confidence in the reported insights.

### Findings

* Approximately **2%** of Truck IDs were missing.
* Approximately **2%** of Driver IDs were missing.
* Approximately **2%** of Trailer IDs were missing.
* Missing values were randomly distributed across the dataset.
* One blank Truck ID was excluded from truck-level comparisons.
* 120 trucks were registered.
* 92 trucks recorded operational activity.
* 28 inactive trucks still incurred maintenance costs.
* All trip records were marked as **Completed**.

These findings were documented and considered throughout the analysis.

---

# ⚠ Challenges & Solutions

## Challenge 1

**Maintenance records could not be directly linked to operational fact tables.**

### Solution

Maintenance records did not share a transactional key with Trips or Loads. Instead of forcing an inaccurate relationship, maintenance analysis was treated independently while operational metrics were calculated from the merged fact table.

---

## Challenge 2

**Some dashboard visuals were not fully interactive because of model limitations.**

### Solution

The dashboard was redesigned by replacing visuals dependent on disconnected tables with business questions answerable from the merged operational dataset, preserving interactivity and analytical value.

---

## Challenge 3

**Inactive trucks incurred maintenance costs despite having no operational activity.**

### Solution

The fleet master contained 120 registered trucks, but only 92 recorded operational activity during the analysis period. Rather than including all registered trucks in performance metrics, operational KPIs were calculated using active trucks identified from the Trips, Loads, and Fleet Utilization tables. The remaining 28 inactive trucks were documented separately, highlighting that non-operational assets can still generate maintenance expenses.

---

# 📈 Key Findings & Recommendations

### **1. Fleet Utilization**

**Finding:** Fleet utilization remained stable at approximately **83%**, indicating consistent use of available fleet capacity.

**Recommendation:** Maintain current asset allocation while investigating opportunities to improve utilization of inactive or underutilized trucks to maximize fleet productivity.

---

### **2. Financial Performance**

**Finding:** Revenue consistently exceeded operating costs throughout the reporting period, demonstrating sustained operational profitability.

**Recommendation:** Continue monitoring operating costs, particularly fuel and maintenance expenses, to preserve profit margins as operations scale.

---

### **3. Customer Service**

**Finding:** The average **On-Time Delivery Rate was 44.6%**, indicating that more than half of deliveries missed their scheduled delivery window.

**Recommendation:** Investigate delivery delays by route, facility, or operational process, and implement corrective actions to improve service reliability and customer satisfaction.

---

### **4. Maintenance**

**Finding:** Preventive (16.8%) and Repair (16.5%) activities represented the largest share of maintenance work, while Inspections accounted for only **3.8%**.

**Recommendation:** Increase preventive inspection frequency to detect issues earlier and reduce costly corrective repairs and unexpected downtime.

---

### **5. Safety & Risk**

**Finding:** The Top 10 cities accounted for **71%** of all incidents, with **68%** classified as Moderate or Severe.

**Recommendation:** Prioritize safety initiatives, driver training, and operational audits in high-risk cities to reduce incident frequency and severity.

---

### **6. Customer Demand**

**Finding:** The Top 10 customers accounted for only **5.6%** of total deliveries, indicating a well-diversified customer portfolio.

**Recommendation:** Maintain strong service levels across the customer base while identifying opportunities to deepen relationships with high-volume customers.

---

### **7. Facility Operations**

**Finding:** The Top 10 facilities handled **20.6%** of total loads, while workloads remained relatively balanced across the network.

**Recommendation:** Continue monitoring facility capacity to ensure balanced resource allocation and identify locations that may require additional operational support as demand grows.





---

# 📂 Repository Structure

```text
excel-logistics-operations-dashboard
│
├── README.md
├── LICENSE
│
├── Dashboard
│   └── Logistics_Operations_Dashboard.xlsx
│
├── Images
│   ├── Dashboard.png
│   ├── Executive_Insight.png
│   ├── Report_Page.png
│   └── Data_Model.png
│
└── Documentation
    ├── Business_Requirements_Document.pdf
    ├── Executive_Insights_Report.pdf
    └── Operational_Report.pdf
```

---

# 📚 Skills Demonstrated

* Business Intelligence
* Data Cleaning
* Data Modeling
* DAX
* Dashboard Design
* Data Storytelling
* KPI Development
* Executive Reporting
* Logistics Analytics
* Data Validation
* Business Analysis

---

# 🔄 Project Workflow

```text
Business Requirements
        │
        ▼
Data Cleaning (Power Query)
        │
        ▼
Data Modeling (Power Pivot)
        │
        ▼
DAX Measure Development
        │
        ▼
Interactive Dashboard Design
        │
        ▼
Executive Insight Development
        │
        ▼
Business Recommendations
```

---

# 📸 Dashboard Gallery

## Fleet Operations Dashboard

*(Insert Dashboard screenshot)*

## Executive Insight

*(Insert Executive Insight screenshot)*

## Operational Report

*(Insert Report Page screenshot)*

---

# 💼 Business Value

This dashboard enables logistics managers to:

* Monitor operational performance from a single interface.
* Compare revenue against operating costs.
* Track fleet utilization and downtime.
* Evaluate delivery reliability.
* Optimize maintenance planning.
* Identify operational risks.
* Support faster, data-driven decision-making.

---

# 👩‍💻 About the Author

**Ijeoma Lorretta, Anya**

Operations & Data Analyst

I enjoy transforming operational data into meaningful insights that support better business decisions. My interests include logistics analytics, supply chain performance, business intelligence, and dashboard design.

**Connect with me:**

* **LinkedIn:** https://www.linkedin.com/in/ijeoma-lorretta-anya
* **GitHub:** https://github.com/LiaBfab

---

# ⭐ If you found this project useful...

If you found this project interesting or helpful, consider giving the repository a **⭐ Star** or connecting with me on LinkedIn.



