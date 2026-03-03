Here is the simplified, text-only version of your README.

---

# NYC Taxi Data - Analytics Engineering with dbt

This project demonstrates data modeling best practices using dbt (data build tool) to transform raw New York City Taxi and Limousine Commission (TLC) data into clean, actionable insights.

### Project Overview

The goal of this project is to build a robust data pipeline that transforms raw taxi trip data into structured analytical models. We follow a modular architecture to ensure data quality, reusability, and scalability.

### Data Architecture

The data model is organized into three distinct layers:

1. **Staging (stg_)**: The entry point for raw data. Here, we perform basic cleaning, renaming columns for consistency, and casting data types.
2. **Intermediate (int_)**: The transformation layer where we apply business logic, join staging models, and perform complex calculations.
3. **Marts (fct_ / dim_)**: The final reporting layer. These models are optimized for BI tools and end-user analysis, such as Fact tables for trips and Dimension tables for locations.

### Tech Stack

* dbt: For data transformation and modeling.
* SQL: The core language for transformations.
* Data Warehouse: Support for platforms like BigQuery, Snowflake, or Postgres.

### Project Structure

```text
models/
├── staging/      # Raw data cleaning
├── intermediate/ # Business logic and joins
└── marts/        # Final analytics-ready tables

```

### Getting Started

1. **Clone the repository**:
```bash
git clone https://github.com/Olapels/analytics_engineering_with_dbt.git

```


2. **Install dbt dependencies**:
```bash
dbt deps

```


3. **Run the models**:
```bash
dbt run

```


4. **Test the data**:
```bash
dbt test

```



### Resources

* Learn more about dbt [in the docs](https://docs.getdbt.com/docs/introduction).
* Check out the [NYC Taxi and Limousine Commission](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page) for dataset details.
