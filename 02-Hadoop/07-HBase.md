# HBase

- Column-oriented non-relational database management system
- HBase runs on top of Hadoop
- Provides a fault-tolerant way of storing sparse datasets
- Works well with real-time data and random read and write access to Big Data

## HBase Features

- HBase is used for write heavy applications
- HBase is linearly and modularly scalable
- It is a backup support for MapReduce jobs
- It provides consistent reads and writes
- It has no fixed column schema
- It is an easy-to-use java API for client access
- It provides data replication across cluster

### Few things to note
- Predefine the table schema and specify column families
- New columns can be added to column families at anytime
- HBase schema is very flexible
- HBase has master nodes to manage the cluster and region servers to perform the work