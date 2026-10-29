# Walmart Retail Data Engineering Pipeline

An end-to-end data engineering project focused on building a scalable retail data pipeline using Apache Airflow, Python, SQL, dbt, PostgreSQL, AWS S3, Docker, and Databricks.

## Project Overview

This project explores the development of a modern retail data pipeline to ingest, store, transform, and prepare Walmart retail data for analytics. It follows a lakehouse-oriented approach, with an emphasis on modular transformations, workflow orchestration, and data quality.

## Tech Stack

- **Programming:** Python, SQL
- **Workflow Orchestration:** Apache Airflow
- **Data Transformation:** dbt
- **Data Platform:** Databricks
- **Database:** Neon PostgreSQL
- **Object Storage:** AWS S3
- **Containerization:** Docker
- **Architecture:** Lakehouse / Medallion Architecture

## Architecture

The intended workflow is:

1. **Data Ingestion:** Load retail data from the project's configured data source(AgenticDB).
2. **Bronze Layer:** Store raw ingested data.
3. **Silver Layer:** Clean, validate, and standardize data.
4. **Gold Layer:** Prepare curated datasets for reporting and analytics.
5. **Orchestration:** Use Apache Airflow to schedule and coordinate pipeline tasks.
6. **Transformation and Quality:** Use dbt models and tests to structure transformations and validate data.
7. **Storage and Analytics:** Use PostgreSQL and/or AWS S3 for configured storage and Databricks for analytics as integration progresses.

*Note: The Silver and Gold layers and Databricks workflow should be marked as implemented only after they are working in the project.*

## dbt Implementation

The dbt project includes:

- 13 dbt models
- 5 snapshots
- 5 data tests

These support modular data transformations, historical data tracking, and data quality checks.


## Environment Configuration

Create a local `.env` file using `.env.example` as a template.

```env
DATABRICKS_HOST=
DATABRICKS_WORKSPACE_ID=
DATABRICKS_TOKEN=
```

Add other required environment variables for PostgreSQL, AWS, Airflow, and the data source as needed.

**Security:** Never commit `.env`, access tokens, database passwords, AWS access keys, or other secrets to GitHub. Store actual credentials locally or in an appropriate secrets manager.

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/DHARANESH-007/walmart-retail-data-engineering-databricks.git
cd walmart-retail-data-engineering-databricks
```

### 2. Configure environment variables

Create your `.env` file and supply the required credentials locally.

### 3. Start the configured Docker services

```bash
docker compose up -d
```

### 4. Run the pipeline

Use the configured Airflow interface to enable and trigger the relevant DAGs. Run dbt transformations using the project's configured profile and target.

*Exact setup steps depend on the final Docker Compose, Airflow, and dbt configuration.*

## Key Features

- Scheduled workflow orchestration with Apache Airflow
- Modular SQL transformations with dbt
- Data quality testing and historical snapshots
- AgenticDB data storage
- AWS S3 integration where configured
- Containerized development environment with Docker
- Databricks workspace configuration for planned or ongoing integration

## Future Improvements

- Complete Databricks integration with the Airflow workflow
- Implement and validate end-to-end Bronze, Silver, and Gold processing
- Add monitoring, logging, and failure notifications
- Improve automated data quality checks
- Build analytical dashboards and business-focused retail metrics

## Author

**Dharanesh D B**

GitHub: [DHARANESH-007](https://github.com/DHARANESH-007)
