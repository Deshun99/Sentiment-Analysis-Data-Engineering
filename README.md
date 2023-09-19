# Singapore Stock Market Data Warehouse

## Overview
Provide retail investors with a consolidated, user-friendly platform for analyzing Singapore's stock market data, enabling more informed investment decisions.

## Main Components
- **Google BigQuery**: The primary data warehouse solution.
- **Apache Airflow**: Orchestrating ETL pipelines.

## Rationale Behind Using Google BigQuery

### 1. Performance
- Offers high-speed SQL queries.
- Interactive analysis of vast datasets.

### 2. Architecture
- Uses shared-nothing architecture (SN).
- Efficient data storage in distributed units and processing.

### 3. Scalability
- Serverless nature.
- Automatic provisioning of compute resources.

### 4. Consistency
- ACID-compliant ensuring data reliability.

## ACID vs BASE
- **CAP Theorem Implication**: Consistency and availability trade-off.
  - Retail investors need **consistent and predictable data**.
  - BASE's eventual consistency can present **outdated data during reads**.

## Cloud vs Traditional Databases
- **Performance**: Superior in cloud solutions like BigQuery.
- **Elasticity**: Manual resource allocation needed in databases like PostgreSQL.
- **Cost**: Pay-per-use with no operational overhead in cloud solutions.
- **Fault-Tolerance**: Replicated data ensures no single point of failure.

## Comparison: BigQuery vs Snowflake vs Amazon Redshift

### BigQuery
- Simplified setup.
- Superior performance on large datasets.
- Economic for sporadic query nature.

### Redshift
- Needs tuning.
- Requires hands-on management due to coupled compute and storage.

### Snowflake
- Similar to BigQuery in many aspects.
- More expensive considering our use case's sporadic query nature.

