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