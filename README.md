# Last-Mile Delivery Analysis | Power BI

## Project Overview

This project focuses on analysing last-mile delivery operations using Microsoft Power BI. The objective is to transform raw operational data into meaningful business insights by examining delivery demand, customer behaviour, delivery performance, driver and vehicle performance, and delivery-related problems.

The project follows an end-to-end data analytics workflow, including data cleaning, data modelling, DAX calculations, and interactive dashboard development.

## Tools & Technologies

- Microsoft Power BI
- Power Query
- DAX (Data Analysis Expressions)
- Data Modelling
- Data Visualisation

## Project Objectives

- Analyse order demand across delivery zones and service types.
- Understand customer ordering behaviour.
- Evaluate delivery completion and failure rates.
- Examine driver workload and vehicle usage.
- Identify repeated delivery attempts and delivery problems.
- Provide data-driven business recommendations.

## Dataset Structure

The project uses six main tables:

| Table | Description |
|---|---|
| Customers | Customer information and customer categories |
| Orders | Order details, priority, service type, and order value |
| Deliveries | Delivery records, status, attempts, and duration |
| Drivers | Driver details and ratings |
| Vehicles | Vehicle information and specifications |
| date_table | Calendar information for time-based analysis |

The model contains two fact tables (Orders and Deliveries) and supporting dimension tables.

## Data Cleaning – Power Query

The following data-cleaning operations were performed:

- Removed genuine duplicate records.
- Used Trim and Clean to standardise text fields.
- Standardised categorical values.
- Replaced selected missing categorical values with "Unknown".
- Corrected column data types.
- Inspected missing values and data quality.
- Preserved meaningful null values, including missing actual delivery dates for records without a completed delivery.

## Data Modelling

The model uses relationships between Customers, Orders, Deliveries, Drivers, Vehicles, and the Date table.

Two fact tables are maintained because order-level and delivery-level records represent different levels of detail.

An inactive relationship involving actual delivery date is used in specific calculations when analysing completed deliveries by actual delivery date.

## DAX & Measures

DAX measures were organised into five logical measure tables:

1. Delivery Demand
2. Customer Order Behaviour
3. Delivery Performance
4. Driver and Vehicle Performance
5. Delivery Problems

Important calculations include:

- Total Orders
- Total Order Value
- Average Order Value
- Delivery Completion Rate
- Failed Delivery Rate
- Average Delivery Duration
- Orders per Customer
- Repeat Customer Rate
- Deliveries per Driver
- Vehicle Utilisation Rate
- Multiple-Attempt Delivery Rate
- Month-over-Month Order Growth

## Power BI Dashboards

### 1. Delivery Demand Analysis
Analyses order volume by delivery zone, service type, priority, and month.

### 2. Customer Behaviour Analysis
Examines customer categories, customer ordering frequency, customer value, and repeat ordering behaviour.

### 3. Delivery Performance Analysis
Evaluates delivery status distribution, completion rate, failed deliveries, and delivery duration.

### 4. Driver and Vehicle Performance
Analyses driver workload, driver ratings, and vehicle usage by type.

### 5. Delivery Problems Analysis
Examines failed delivery records, multiple attempts, and delivery-attempt patterns.

### 6. Executive Summary
Provides a consolidated overview of the major operational KPIs and business findings.

## Key Business Findings

- Approximately 3K unique orders were analysed.
- Approximately 4K delivery records were analysed.
- Total order value was approximately 7.52M.
- ZONE0005 recorded the highest order volume among the five leading zones, with 240 orders.
- Standard delivery recorded the highest service-type order count, with 620 orders.
- Business customers contributed 68.33% of orders.
- Delivery completion rate was 73.74%.
- Failed delivery rate was 8.43%.
- Average delivery duration was 47.19 minutes.
- There were 295 failed delivery records and 165 multiple-attempt records.

*Note: Repeat customer rate and vehicle utilisation are reported dashboard metrics and require validation of their calculation definitions before being interpreted as customer retention or full operational utilisation.*

## Business Recommendations

- Investigate failed, pending, and rescheduled delivery records.
- Monitor high-demand delivery zones.
- Review demand distribution across service types.
- Understand the ordering behaviour of business customers.
- Monitor driver workload distribution.
- Validate vehicle utilisation calculations.
- Investigate multiple-attempt delivery records to identify improvement opportunities.

## Project Files

- Power BI report (`.pbix`)
- Dashboard screenshots
- Project presentation

## Conclusion

This project demonstrates the use of Power BI for end-to-end data analysis, from data preparation and modelling to DAX calculations and interactive dashboard development. It highlights how operational data can be transformed into business insights to support data-driven decision-making.

**Developed as a Data Analytics portfolio project.**
