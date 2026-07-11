# Weather Data Engineering Project

Real-time weather pipeline demonstrating incremental loading,
SCD2, dbt snapshots, and forecast vs actuals analytics.

## Data Source
Open-Meteo API — free, no API key required

## Stack
- Ingestion: Python + requests
- Storage: AWS S3 (data lake) + Snowflake (warehouse)
- Transformation: dbt Core (incremental models + snapshots)
- Orchestration: Apache Airflow
- CI/CD: GitHub Actions

## Architecture
API → S3 → Snowflake RAW → dbt → MARTS

## Environments
| Branch     | Snowflake DB     |
|------------|------------------|
| feature/*  | WEATHER_DEV      |
| develop    | WEATHER_STAGING  |
| main       | WEATHER_PROD     |
