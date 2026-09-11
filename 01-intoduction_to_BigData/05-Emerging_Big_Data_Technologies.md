# Emerging Big Data Technologies

## 1. Apache Pulsar
- Open-source, cloud-native messaging and streaming platform.
- Designed for high-throughput and low-latency data.
- Supports both message queues and real-time streaming in one system.
- Supports multi-tenancy, meaning multiple teams/apps can use the same cluster with isolation.
- Has built-in geo-replication for distributing data across locations.
- Separates compute and storage, helping it scale horizontally.
**Main uses:** real-time data pipelines, event-driven applications/microservices, and real-time analytics pipelines.
**Limitations:** harder to deploy/manage and has a smaller ecosystem than Kafka.

## 2. Apache Druid
- A real-time analytics database.
- Best suited for event-driven and time-series data, such as logs, metrics, and clickstreams.
- Uses columnar storage, which makes filtering and aggregation fast.
- Can ingest both streaming and batch data.
- Optimized for OLAP (Online Analytical Processing).
- Can scale horizontally to handle very large datasets.
**Main uses:** interactive dashboards, fraud detection, trend/anomaly detection, and operational analytics.
**Limitations:** complex setup and less flexible for non-time-series data.

## 3. PrestoDB
- An open-source distributed SQL query engine.
- Designed to execute SQL queries on very large datasets at interactive speeds.
- Can query multiple sources such as HDFS, S3, MySQL and NoSQL databases.
- Supports federated queries — one query can combine data from different systems.
- This can reduce the need to move all data through ETL before querying it.
**Main uses:** data lake queries, BI/reporting, interactive analytics and ad-hoc data exploration
**Limitation:** not intended for transaction processing or streaming and may need tuning for large queries

## Important Comparison

| Technology | Main Purpose | Latency |
|------------|--------------|---------|
| Hadoop | Large-scale batch/ETL processing | High |
| Spark | Batch + stream processing | Low |
| Pulsar | Messaging + streaming | Low |
| Druid | Real-time analytics | Low |
| PrestoDB | SQL queries across data sources | Low |

## Most important thing to remember

- Pulsar → Streaming & Messaging
- Druid → Real-time Analytics
- PrestoDB → Fast SQL Queries
- Spark → Data Processing
- Hadoop → Batch Processing