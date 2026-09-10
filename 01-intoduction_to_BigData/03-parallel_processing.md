# Parallel processing and scalability

## Linear vs Parallel processing





        Linear processing                         Parallel processing


           ┌─────────────┐                                ┌─────────────┐
           │   Problem   │                                │   Problem   │
           └──────┬──────┘                                └──────┬──────┘
                  │                                        ╱     │     ╲
                  ▼                                       ╱      │      ╲
           ┌─────────────┐                               ▼       ▼       ▼
           │Instruction 1│                  ┌────────────┐ ┌────────────┐ ┌────────────┐
           └──────┬──────┘                  │Instruction1│ │Instruction2│ │InstructionN│
                  │                         └──────┬─────┘ └──────┬─────┘ └──────┬─────┘
                  ▼                                ╲              │              ╱
           ┌─────────────┐                          ╲             │             ╱
           │Instruction 2│                           ╲            │            ╱
           └──────┬──────┘                            ╲           ▼           ╱
                  │                                    ╲    ┌─────────────┐  ╱
                  ▼                                     ───▶│   Output    │◀─
           ┌─────────────┐                                  └─────────────┘
           │Instruction N│
           └──────┬──────┘
                  │
                  ▼
           ┌─────────────┐
           │   Output    │
           └─────────────┘


## Advantages of Parallel Processing

- parallel processing approach can process large datasets in a fraction of time
- Less memory and compute requirements needed as set of instructions are distributed to smaller execution nodes
- More execution nodes can be added or removed from processing network depending on complexity of the problem

## Data scaling in Big Data

- Data scaling is a technique to manage, store and process the overflow of data
- Increasing the capacity of a single node as means of increasing capacity is called scaling up

## Fault tolerance

- The ability of system to continue operating without interruption when one or more of its components fail


## Horizontal Scaling / Scaling Out

- Adding more machines or nodes to handle the increased workload, improving capacity and flexibility

## Embarrassingly Parallel

- Calculations easily divide workloads that run independent of one another
- If any one process fails, it has no impact on the others and can simply be rerun