# MapReduce

- Programming model used in Hadoop for processing Big Data
- Processing technique for distributed computing 
- Consists of a Map task and a Reduce task
- Can be coded in many programming language like Java, C++, Python, Ruby, and R

**Distributed Computing is a system with multiple components located on different machines that communicate actions in one view to the end user**

## Map and Reduce

- MapReduce framewok contains two tasks, Map and Reduce

### Map     

- Takes an input file and performs mapping tasks by processing and extracting important data information into a key value pairs and these are the preliminary output list

- These outputs further sent to Reducer

### Reducer

- Aggregates and computes a set of result and produces a final output

**MapReduce keeps track of its task by creating a unique key**

## How MapReduce Works

| Input | Split | Map | Shuffle | Reducer | Output |
|---|---|---|---|---|---|
| Teju,<br>Briana,<br>Shannon,<br>Vivek,<br>Vivek, Teju,<br>Briana, Teju | Teju, Briana | Teju 1<br>Briana 1 | Teju [1,1,1] | Teju, 3 | Teju, 3<br>Briana, 2<br>Vivek, 2<br>Shannon, 1 |
| | Shannon, Vivek | Shannon 1<br>Vivek 1 | Briana [1,1] | Briana, 2 | |
| | Vivek, Teju | Vivek 1<br>Teju 1 | Vivek [1,1] | Vivek, 2 | |
| | Briana, Teju | Briana 1<br>Teju 1 | Shannon [1] | Shannon, 1 | |

## Why use MapRedce?

- Parallel computing
- Divide ---> Run Task ---> Done
- Process data in tabular and non tabular forms such as videos
- Support for multiple languages
- Platform for analysis and data ware housing

## Common use cases

### 1. Social Media

- Social Media platforms can use MapReduce to analyze who visited your profile and who viewed your posts (LinkedIn, Instagram)

### 2. Reccomendations

- Create a recommender system for users and provide suggestions for them based on their interest (Netflix)

### 3. Financial Industries

- Can be used for fraud detection by analyzing behaviors of buyers and tracking down anomalies

### 4. Advertisement

- Can be used for analyze and understand the interaction with ads and the engagement levels