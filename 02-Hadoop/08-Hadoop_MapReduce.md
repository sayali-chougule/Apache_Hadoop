# Set up Single-Node Hadoop

1. Download hadoop-3.2.3.tar.gz to your theia environment by running the following command

```sh
curl https://dlcdn.apache.org/hadoop/common/hadoop-3.3.6/hadoop-3.3.6.tar.gz --output hadoop-3.3.6.tar.gz
```

2. Extract the tar file in the currently directory

```sh
tar -xvf hadoop-3.3.6.tar.gz
```

3. Navigate to the hadoop-3.3.6 directory

```sh
cd hadoop-3.3.6
```

4. Check the hadoop command to see if it is setup. This will display the usage documentation for the hadoop script

```sh
bin/hadoop
```

5. Run the following command to download data.txt to your current directory

```sh
curl https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-BD0225EN-SkillsNetwork/labs/data/data.txt --output data.txt
```

6. Run the Map reduce application for wordcount on data.txt and store the output in /user/root/output

```sh
bin/hadoop jar share/hadoop/mapreduce/hadoop-mapreduce-examples-3.3.6.jar wordcount data.txt output
```

7. Once the word count runs successfully, you can run the following command to see the output file it has generated

```sh
ls output
```

**You should see part-r-00000 with _SUCCESS indicating that the wordcount has been done**

8. Run the following command to see the word count output.

```sh
cat  output/part-r-00000
```

The image below shows how the MapReduce wordcount happens

![MapReduce](MapReduce.png)