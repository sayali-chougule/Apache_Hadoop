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