# fabric_sales_project
# Microsoft Fabric Sales Analytics Project

## About the Project

This project demonstrates an end-to-end sales analytics solution built using Microsoft Fabric and Power BI.

The solution follows the **Medallion Architecture**, where data moves through Bronze, Silver, and Gold layers before being used for reporting.

### Data Flow

**Source Data → Dataflow Gen2 → Bronze → Silver → Gold → Semantic Model → Power BI**

### What I Built

* Used **Dataflow Gen2** to ingest and transform the source data.
* Implemented **Bronze, Silver, and Gold layers** to organize the data processing workflow.
* Cleaned and standardized data in the **Silver layer**.
* Created business-ready tables in the **Gold layer**.
* Built a **semantic model** using fact and dimension tables.
* Created **DAX measures** for sales analysis and KPIs.
* Developed an interactive **Power BI sales dashboard**.
* Documented the architecture and implementation in GitHub.

### Technologies

* Microsoft Fabric
* Dataflow Gen2
* OneLake
* Lakehouse
* Semantic Model
* DAX
* Power BI
* GitHub

### Business Analysis

The Power BI report provides insights into:

* Total Sales
* Total Orders
* Sales by Year
* Monthly Sales Trends
* Sales by Product
* Sales by Customer
* Year-over-Year Sales Growth

### Project Goal

The goal of this project is to demonstrate how Microsoft Fabric can be used to build a complete data and BI solution, from data ingestion and transformation to semantic modeling and business reporting.
