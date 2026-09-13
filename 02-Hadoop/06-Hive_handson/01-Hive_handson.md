### In this lab, created a table in hive, added data to the table from csv and listed the data contained in the table.



## Step 1: Get a copy of the CSV file

1. Create a directory named data under project directory by running the following command

```sh
mkdir project_dir/data
```

2. Change to the data directory

```sh
cd project_dir/data
```

3. Run the following command to get the emp.csv, a data file with Employee data, in a comma-separated file.

```sh
wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-BD0225EN-SkillsNetwork/data/emp.csv
```

4. Open the file in editor and view the file

## Step 2: Setup Hive and Bee

1. Pull the hive image into system by running the following command

```sh
docker pull apache/hive:4.0.0-alpha-1
```

2. Run the hive server on port ```10002```. Name the server instance ```myhiveserver```. Mount the local ```data``` folder in the hive server as ```hive_custom_data```. This would mean that the whole ```data``` folder that created locally, along with anything added in the data folder, is copied into the container under the directory hive_custom_data

```sh
docker run -d -p 10000:10000 -p 10002:10002 --env SERVICE_NAME=hiveserver2 -v /home/project/data:/hive_custom_data --name myhiveserver apache/hive:4.0.0-alpha-1
```

3. Run the following command, which allows to access ``beeline``. This is a SQL cli where we can create, modify, delete table, and access data in the table

```sh
docker exec -it myhiveserver beeline -u 'jdbc:hive2://localhost:10000/'
```

## Step 3: Create table, add and view data

1. To create a new table Employee with three columns as in the csv downloaded - em_id, emp_name and salary, run the following command

```sh
create table Employee(emp_id string, emp_name string, salary  int)  row format delimited fields terminated by ',' ;
```

2. Run the following command to check if the table is created.

```sh
show tables;
```
This should list the Employee table that just created

3. Now load the data into the table from the csv file by running the following command.

```sh
LOAD DATA INPATH '/hive_custom_data/emp.csv' INTO TABLE Employee;
```

4. Run the following command to list all the rows from the table to check if the data has been loaded from the CSV.

```sh
SELECT * FROM employee;
```

5. To quit from the beehive prompt in the terminal, press ``ctrl+D``

Hive internally uses MapReduce to process and analyze data. When we execute a Hive query, it generates MapReduce jobs that run on the Hadoop cluster.



