Automated Excel ETL & Business Monitoring Dashboard

Project Overview

This project is an end-to-end Excel-based ETL and business monitoring system built using Power Query. I designed it to simulate a real-world multi-city quick commerce and subscription business where operational data comes from multiple sources and needs to be consolidated, validated, and analyzed automatically.

The goal of this project was not just to build a dashboard, but to create a structured data pipeline inside Excel where business users can simply update raw files and click Refresh All to get updated insights.

⸻

Business Problem

In many operational businesses, data comes from different systems such as order management, payment systems, subscription databases, and vendor records. These files are often separate, inconsistent, and difficult to analyze together.

Common challenges include:

	•	Orders without payment
	•	Expired subscriptions still generating orders
	•	Loss-making sales
	•	Inconsistent data formats
	•	Manual consolidation errors

This project solves these issues by building a layered ETL system inside Excel.

⸻

Data Sources

The system processes four raw files.

Daily Orders

	•	Order_ID
	•	Order_Date
	•	City
	•	Product_Name
	•	Quantity
	•	Order_Value
	•	Customer_ID

Payment Reconciliation

	•	Transaction_ID
	•	Order_ID
	•	Payment_Mode
	•	Payment_Status
	•	Paid_Amount

Subscription Customers

	•	Customer_ID
	•	Plan_Type
	•	Start_Date
	•	End_Date
	•	Status

Vendor Supply

	•	Vendor_ID
	•	Product_Name
	•	Cost_Price
	•	Supply_Date
	•	City

Each file is ingested through a folder-based connection to allow scalable refresh.

⸻

ETL Architecture

I implemented a layered approach using Power Query.

Staging Layer (stg_)

Raw data is imported directly from the folder without modification.

Cleaning Layer (clean_)

	•	Standardized date formats
	•	Validated numeric fields
	•	Removed duplicates
	•	Handled null values
	•	Applied data consistency checks

Fact Layer (fact_)

	•	Consolidated order-level data
	•	Merged payment status
	•	Validated subscription activity
	•	Compared cost vs revenue to detect loss-making orders

All transformations are handled inside Power Query. No manual editing is required.

⸻

Exception Logic

A key part of this project is automated exception reporting. The system automatically identifies:

	•	Orders without payment
	•	Orders from inactive subscriptions
	•	Loss-making orders
	•	Revenue at risk

These exception tables update automatically when data is refreshed.

⸻

Dashboard Features

The executive dashboard includes:

	•	Total Orders
	•	Total Revenue
	•	Average Order Value
	•	Revenue at Risk percentage
	•	Orders vs Revenue by City
	•	Monthly trend analysis
	•	Exception volume overview

It also includes:

	•	City slicer
	•	Month slicer

All visuals update automatically after clicking Refresh All.

⸻

How to Use
	1.	Replace the raw files inside the designated Raw Data folder.
	2.	Open the Excel dashboard file.
	3.	Click Data → Refresh All.

The ETL process runs automatically and updates all KPIs, charts, and exception reports.

No formulas need to be modified.

⸻

Skills Demonstrated

	•	Excel ETL design using Power Query
	•	Data cleaning and transformation
	•	Fact-based data modeling
	•	Exception reporting logic
	•	KPI design and executive dashboard development
	•	Scalable folder-based refresh architecture


⸻

Conclusion

This project demonstrates how Excel can be used as a structured analytics platform when combined with Power Query and proper data modeling practices. The final solution provides a practical, refresh-driven business monitoring system suitable for operational decision-making.
