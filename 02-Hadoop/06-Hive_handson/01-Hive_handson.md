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