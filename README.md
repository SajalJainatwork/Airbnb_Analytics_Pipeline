🚀 End-to-End Data Engineering Project | Airbnb Analytics Pipeline
![bnb](https://github.com/user-attachments/assets/8dba23a0-b9d7-4d43-a284-f480b5fa8296)


![airbnb](https://github.com/user-attachments/assets/c1a19d54-0b40-4160-9d7a-6669f5f2e518)


Built an end-to-end data pipeline that takes raw Airbnb CSV data and turns it into analytics-ready models using AWS S3, dbt, and Snowflake, following production-style warehouse patterns.
What I actually implemented:
• Medallion Architecture
Bronze: Raw CSV ingestion from S3 with minimal transformations
Silver: Deduplication, data standardization, and business logic
Gold: Analytics-ready fact & dimension models (OBT + star schema)
• Metadata-driven transformations
Central pipeline config table (load_type, watermark_column, is_active)
dbt + Jinja used to dynamically control incremental logic without rewriting SQL per model
• Incremental processing
Incremental models using is_incremental() to process only new or changed records
Reduced unnecessary Snowflake compute on reruns
• Historical tracking
Implemented SCD Type 2 dbt snapshots to track changes in entities like listings and hosts
• Data quality enforcement
dbt tests for uniqueness, not-null constraints, and business rules to protect downstream analytics
Tech Stack:
AWS S3 | Snowflake | dbt Core | SQL | Jinja | Python

This project forced me to think beyond “writing SQL” and focus on scalability, cost efficiency, and data reliability, similar to how pipelines behave in real production environments.



