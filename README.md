## Project Summary for GitHub

### Real-Time KPI Computation for RetailCorp Inc.

This project focuses on computing various Key Performance Indicators (KPIs) for an e-commerce company, RetailCorp Inc., using real-time sales data from Kafka. The project follows a specific architecture to process, analyze, and store the data, providing valuable insights into global sales trends and consumer behavior.

### Project Overview

The primary tasks in this project are:

1. **Reading Sales Data from Kafka**: The sales data is streamed in real-time from a Kafka server. The data includes information about invoices, products, and transactions.
2. **Preprocessing the Data**: Additional columns such as `total_cost`, `total_items`, `is_order`, and `is_return` are derived from the raw data.
3. **Calculating KPIs**: KPIs are calculated based on time (one-minute intervals) and both time and country.
4. **Storing KPIs**: The calculated KPIs are stored in JSON files for further analysis. Separate JSON files are created for time-based KPIs and time- and country-based KPIs, which are then zipped for easy access and archival.

### Project Components

- **Python Script**: `spark-streaming.py`
  - This script contains the code for reading the input data streams from Kafka, preprocessing the data, and calculating the KPIs. Proper comments are included to explain each step.
  
- **Documentation**: `CodeLogic.pdf`
  - This document details the logic applied to solve the project, including the commands used to run the Spark Submit job and any other commands used.

- **Output Files**:
  - `Output.zip`: Contains the console output from the Spark Submit command, summarizing the input tables for various batches.
  - `Timebased-KPI.zip`: Contains JSON files for time-based KPIs.
  - `Country-and-timebased-KPI.zip`: Contains JSON files for country- and time-based KPIs.

### How to Run the Project

1. **Set Up EMR Cluster**: Ensure you have an EMR cluster configured similarly to the Apache Spark Streaming module.
2. **Run the Spark Submit Command**: Use the provided commands in the `CodeLogic.pdf` to execute the Spark job.
3. **Check the Outputs**: Verify the outputs in the console and the generated JSON files.


### Acknowledgement

The data used in this project is based on the Online Retail Data Set from the UCI Machine Learning Repository, published by Dr. Daqing Chen, Director of the Public Analytics group.

This project demonstrates the power of big data tools in improving business performance by analyzing trends and consumer behavior, offering better and more customized products to digitally enabled customers worldwide.
