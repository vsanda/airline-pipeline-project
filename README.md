# ✈️ Airline Pipeline Project

## Modular Data Stack for Simulating Airline Profitability

This project simulates an end-to-end airline data platform using modular, production-grade architecture. It models complex airline operations — including flight costs, revenue, crew labor, fuel efficiency, and supplier performance — using a mix of real-world APIs and realistic synthetic data.

## Architecture Overview

Each layer is broken out into its own GitHub repository to reflect real-world separation of concerns:

- **Ingestion Layer** ([airline-data-ingestion](https://github.com/vsanda/airline-data-ingestion))  
  Collects a hybrid of real-time aviation data via APIs (e.g., OpenSky) and simulated flight schedules, bookings, aircraft metadata, fuel prices, crew rosters, and supplier logs using Faker.

- **Orchestration Layer** ([airline-airflow-pipeline](https://github.com/vsanda/airline-airflow-pipeline))  
  Uses Apache Airflow to schedule ingestion pipelines and coordinate data freshness across all components.

- **Modeling Layer** ([airline-dbt-models](https://github.com/vsanda/airline-dbt-models))  
  Transforms raw inputs into analytical gold marts, including:
  - Fuel cost calculations by aircraft type and efficiency  
  - Crew payroll cost estimation per flight  
  - Delay attribution by supplier or staffing issues  
  - Flight- and route-level profitability modeling

- **Analytics Layer** ([airline-analytics-superset](https://github.com/vsanda/airline-analytics-layer)) 
  Planned dashboards using HTML and CSV to visualize delay trends, profitability outliers, and operational risk.

## 🔍 Highlights

- Hybrid data: real-time API + simulated entities modeled with high realism  
- Built with open-source tools: dbt, Airflow, pandas, Faker, Superset  
- P&L simulation by flight and route — with joinable cost and revenue facts  
- Modular repos for ingestion, orchestration, modeling, and analytics
