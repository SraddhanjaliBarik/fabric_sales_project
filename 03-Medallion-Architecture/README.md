# Medallion Architecture

This project follows the Medallion Architecture in Microsoft Fabric to organize and transform sales data through three layers: Bronze, Silver, and Gold.

## Architecture

Source Data
↓
Dataflow Gen2
↓
**Bronze Layer**
↓
**Silver Layer**
↓
**Gold Layer**
↓
Semantic Model
↓
Power BI

## Bronze Layer

The Bronze layer stores the raw data as received from the source system.

### Purpose

* Store raw data
* Preserve the original data
* Perform minimal transformation
* Maintain a reliable source for downstream processing

### Example tables

* Bronze_Sales
* Bronze_Customer
* Bronze_Product
* Bronze_Calendar

---

## Silver Layer

The Silver layer contains cleaned and standardized data.

### Transformations

* Removed duplicate records
* Handled missing values
* Standardized column names
* Converted data types
* Cleaned invalid records
* Applied data quality rules

### Example tables

* Silver_Sales
* Silver_Customer
* Silver_Product
* Silver_Calendar

---

## Gold Layer

The Gold layer contains business-ready data optimized for analytics and reporting.

### Purpose

* Create business-ready tables
* Prepare data for reporting
* Apply business logic
* Support the semantic model
* Improve Power BI reporting performance

### Example tables

* FactSales
* DimCustomer
* DimProduct
* DimDate

---

## Data Transformation Flow

### Bronze → Silver

Raw sales data was cleaned and standardized.

### Silver → Gold

The cleaned data was transformed into a dimensional model using fact and dimension tables.

## Business Model

The Gold layer follows a star-schema approach:

FactSales

* DateKey
* CustomerKey
* ProductKey
* SalesAmount
* Quantity

Dimensions:

* DimDate
* DimCustomer
* DimProduct

## Technologies

* Microsoft Fabric
* OneLake
* Lakehouse
* Dataflow Gen2
* Semantic Model
* Power BI
* DAX
