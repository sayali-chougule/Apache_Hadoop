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