# Hadoop Ecosystem

Hadoop Ecosystem is made up of components that support one another

## 1. Ingest Data
### Flume:
- Collects, aggregates, and transfers big data
- Has a simple and flexible architecture based on streaming data flows
- Uses a simple extensible data model that allows for online analytic application

### Sqoop
- Designed to transfer data between relational database system and Hadoop
- Access the database to understand the schema of the data
- Generates a MapReduce application to import or export data


## 2. Store Data
### HBase
- A non-relational database that runs on top of HDFS
- Provides real time wrangling on data
- Stores data as indexes to allow for random and faster access to data

### Cassandra
- A scalable, NoSQL database designed to have no single point of failure

## 3. Analyze Data
### Pig
- Analyzes large amounts of data
- Operates on client side of cluster
- A procedural data flow language

### Hive
- Used for creating a reports
- Operates on server side of cluster
- A declarative programming language (allows users express which data they wish to receive)

## 4. Access Data
### Impala 
- Scalable and easy to use platform for everyone
- No programming skills required

### Hue
- Stands for Hadoop User Experience
- Allows to upload, brows and query the data
- Runs pig jobs and workflow
- Provides editors for several SQL query language like Hive and MySQL 
