# Dataset of Raft-based Database Diagnosis

## Overview

The dataset download link: 

- normal: https://raft-diagnosis.oss-cn-beijing.aliyuncs.com/normal.zip
- leader: https://raft-diagnosis.oss-cn-beijing.aliyuncs.com/leader.zip
- follower: https://raft-diagnosis.oss-cn-beijing.aliyuncs.com/follower.zip
- database: https://raft-diagnosis.oss-cn-beijing.aliyuncs.com/database.zip
- sample: https://raft-diagnosis.oss-cn-beijing.aliyuncs.com/sample.zip

This dataset is mainly designed for root-cause analysis:

- System Fault
  - CPU Bottleneck
  - Memory Bottleneck
  - IO Bottleneck
  - Network Fault
    - Network Delay Increased
    - Network Bandwidth Limited
    - Network Partition
  - Workload Spike
- Database Fault
  - Database Backup
  - Restore Backup
  - Accompany with Slow Query
  - Too Much Background Tasks
  - Configuration Error


## How to use

Use normal/leader/follower/database to train and test (sample is only selected out for empirical study). 

### normal

No fault is injected

### leader:

Inject fault for leader node

- cpu1: CPU Bottleneck
- memory1: Memory Bottleneck
- io1: IO Bottleneck
- network1: Network Delay Increased
- network2: Network Bandwidth Limited
- network3: Network Partition
- workload1: Workload Spike
- export: Database Backup
- import: Restore Backup
- query1: Accompany with Slow Query

### follower:

Inject fault for follower node

- cpu1: CPU Bottleneck
- memory1: Memory Bottleneck
- io1: IO Bottleneck
- network1: Network Delay Increased
- network2: Network Bandwidth Limited
- network3: Network Partition
- workload1: Workload Spike
- export: Database Backup
- import: Restore Backup
- query1: Accompany with Slow Query

### database:

Modify database configuration and run, which means fault is injected throughout the process

- database1: Background Tasks (Compaction)
- database2: Configuration1 (Flush Frequency)
- database3: Configuration2 (Ratio of write memory for rejecting insertion)
- database4: Lock Contention


