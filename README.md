## Project Overview

This repository demonstrates an end-to-end data pipeline that covers the data engineering lifecycle. The pipeline extracts data from a MySQL database hosted on Amazon RDS, transforms it using AWS Glue, and stores it in Amazon S3. The data is then queried via Amazon Athena and visualized using Jupyter Lab. Infrastructure management is handled by Terraform, following Infrastructure as Code (IaC) principles.

## Pipeline Architecture
![Pipeline Architecture](./images/ETL.drawio)

The pipeline consists of the following stages:

1. **Source System (MySQL on RDS):** 
   - A MySQL database hosted on Amazon RDS contains historical purchase and customer data.
   
2. **ETL with AWS Glue:** 
   - **Extract:** Data is retrieved from the RDS MySQL database.
   - **Transform:** Data is transformed into a star schema for easier analysis.
   - **Load:** Transformed data is stored in Amazon S3 in Parquet format.
   
3. **Serving Layer (Amazon Athena):**
   - Data stored in S3 is queried using Amazon Athena.
   
4. **Visualization (Jupyter Lab):**
   - Data insights are visualized using Jupyter Lab and SQL queries on Athena.

5. **Infrastructure as Code (Terraform):**
   - Terraform is used to provision and manage the cloud infrastructure.

## Tools & Technologies

- **Amazon RDS** for relational database hosting.
- **AWS Glue** for ETL operations.
- **Amazon S3** for object storage.
- **Amazon Athena** for querying data.
- **Jupyter Lab** for visualization.
- **Terraform** for infrastructure management.

1. Clone this repository.
2. Follow the instructions in the provided Jupyter notebook to set up and run the pipeline.
3. Use Terraform to manage infrastructure and deploy resources.

This project provides a hands-on example of the data engineering lifecycle using AWS services.

