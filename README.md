# 🎬 Netflix Data Analytics Pipeline

An **end-to-end modern data analytics pipeline** built using **dbt, Snowflake, AWS S3, and SQL**. This project demonstrates how raw Netflix data is transformed into clean, analytics-ready datasets by following industry-standard data engineering practices such as layered modeling, data quality testing, snapshots, reusable macros, and automated documentation.

---

## 🚀 Features

- 📂 **Data Modeling** – Structured raw data into **Staging**, **Intermediate**, and **Mart** layers using dbt.
- ❄️ **Snowflake Integration** – Built scalable analytical models on Snowflake's cloud data warehouse.
- 📊 **Analytics-Ready Data** – Created business-ready tables optimized for reporting and dashboarding.
- 🔄 **Snapshots** – Implemented dbt snapshots to track historical changes in source data.
- 🌱 **Seeds** – Loaded static reference datasets using dbt seed files.
- 🧩 **Reusable Macros** – Developed custom dbt macros to standardize repetitive SQL transformations.
- ✅ **Data Quality Testing** – Added schema and custom tests to ensure data accuracy and consistency.
- 📚 **Auto Documentation** – Generated interactive dbt documentation with complete data lineage.
- ⚡ **Modular SQL Models** – Built maintainable and reusable SQL transformation logic following dbt best practices.

---

## 📂 Project Structure

```
Netflix-Data-Analytics-Pipeline/
│
├── analyses/          # Analytical SQL queries
├── logs/              # dbt execution logs
├── macros/            # Custom reusable dbt macros
├── models/
│   ├── staging/       # Raw data cleaning
│   ├── intermediate/  # Business transformations
│   └── marts/         # Final analytics models
│
├── seeds/             # Static CSV reference data
├── snapshots/         # Historical data tracking
├── target/            # Compiled dbt artifacts
├── tests/             # Custom data quality tests
│
├── dbt_project.yml
├── packages.yml
└── package-lock.yml
```

---

## 🛠 Tech Stack

| Category | Technologies |
|----------|--------------|
| **Data Warehouse** | Snowflake |
| **Transformation** | dbt |
| **Storage** | AWS S3 |
| **Query Language** | SQL |
| **Documentation** | dbt Docs |
| **Data Validation** | dbt Tests |
| **Version Control** | Git & GitHub |

---

## ⚙️ Pipeline Architecture

```
             AWS S3
                │
                ▼
          Raw Netflix Data
                │
                ▼
           Snowflake Tables
                │
                ▼
        dbt Staging Models
                │
                ▼
     dbt Intermediate Models
                │
                ▼
         dbt Mart Models
                │
                ▼
    Analytics & BI Reporting
```

---

## 📋 Data Modeling Layers

### 📌 Staging Layer
- Cleaned and standardized raw Netflix datasets.
- Renamed columns and corrected data types.
- Removed duplicate records.
- Applied basic data cleaning.

---

### 📌 Intermediate Layer

- Applied business transformation logic.
- Created reusable datasets.
- Joined multiple staging models.
- Prepared data for analytical consumption.

---

### 📌 Mart Layer

- Built business-ready fact and dimension tables.
- Optimized datasets for dashboards and reporting.
- Created final analytical models for end users.

---

## 🔄 dbt Components Used

### ✅ Sources
Configured Snowflake source tables to establish a reliable connection between raw datasets and dbt models.

### 🌱 Seeds
Loaded static CSV files into Snowflake for lookup and reference data.

### 📸 Snapshots
Tracked historical changes in source records using dbt snapshots.

### 🧩 Macros
Created reusable SQL macros to eliminate repetitive transformation logic.

### ✅ Tests
Implemented dbt tests including:

- Unique
- Not Null
- Accepted Values
- Relationships
- Custom SQL Tests

to ensure high-quality and reliable data.

### 📚 Documentation
Generated interactive project documentation and data lineage using:

```bash
dbt docs generate
dbt docs serve
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/netflix-data-analytics-pipeline.git

cd netflix-data-analytics-pipeline
```

---

### 2. Install dbt

```bash
pip install dbt-core
pip install dbt-snowflake
```

---

### 3. Configure Snowflake Connection

Update your `profiles.yml` file with your Snowflake credentials.

```yaml
netflix_project:
  target: dev
  outputs:
    dev:
      type: snowflake
      account: YOUR_ACCOUNT
      user: YOUR_USERNAME
      password: YOUR_PASSWORD
      role: YOUR_ROLE
      database: YOUR_DATABASE
      warehouse: YOUR_WAREHOUSE
      schema: YOUR_SCHEMA
      threads: 4
```

---

### 4. Install dbt Packages

```bash
dbt deps
```

---

### 5. Load Seed Data

```bash
dbt seed
```

---

### 6. Run Models

```bash
dbt run
```

---

### 7. Execute Tests

```bash
dbt test
```

---

### 8. Generate Documentation

```bash
dbt docs generate
dbt docs serve
```

---

## 📊 Workflow

```
AWS S3
    │
    ▼
Snowflake Raw Tables
    │
    ▼
dbt Sources
    │
    ▼
Staging Models
    │
    ▼
Intermediate Models
    │
    ▼
Mart Models
    │
    ▼
dbt Tests
    │
    ▼
dbt Documentation
    │
    ▼
Analytics & Reporting
```

---

## 🎯 Learning Outcomes

Through this project, I gained hands-on experience with:

- Building scalable ELT pipelines using dbt.
- Designing layered data models (Staging → Intermediate → Mart).
- Working with Snowflake as a cloud data warehouse.
- Implementing reusable SQL transformations with dbt macros.
- Performing automated data quality testing.
- Tracking historical data using snapshots.
- Generating interactive data lineage and project documentation.
- Applying modern data engineering best practices.

---

## 📌 Future Enhancements

- Integrate AWS Glue for automated data ingestion.
- Schedule pipelines using Apache Airflow.
- Add CI/CD using GitHub Actions.
- Connect Power BI/Tableau dashboards.
- Implement incremental models for large datasets.
- Add data observability and monitoring.

---

## 🧠 Summary

| Category | Tools |
|----------|-------|
| **Cloud Storage** | AWS S3 |
| **Data Warehouse** | Snowflake |
| **Transformation** | dbt |
| **Language** | SQL |
| **Data Validation** | dbt Tests |
| **Historical Tracking** | dbt Snapshots |
| **Reusable Logic** | dbt Macros |
| **Documentation** | dbt Docs |
| **Version Control** | Git & GitHub |
