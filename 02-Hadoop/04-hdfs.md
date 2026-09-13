# HDFS

- Hadoop Distributed File System
- It is a storage layer of Hadoop
- Splits files into blocks, creates replicas of blocks and stores them on different machines
- Provides access to streaming data
- HDFS uses a command line interface to interact with Hadoop

**Streaming means that HDFS provides a constant bitrate when transferring data rather than having the data being transferred in waves**

## Key Features

- **Cost Efficient** - The storage hardware is not expensive
- **Large amount of data** - HDFS can store upto petabytes of data
- **Replication** - Makes pieces of data on multiple machines
- **Fault Tolerant** - If one machine crashes, a copy of the data can be found somewhere else and work continues
- **Scalable** - One cluster can be scaled into hundreds of nodes
- **Portable** - Can easily move across multiple platforms