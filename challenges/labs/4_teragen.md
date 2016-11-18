# Teragen
> time hadoop jar hadoop-examples.jar teragen -D mapreduce.job.maps=8 -D dfs.blocksize=16777216 51200000 /user/bavaria/tgen512m

```
real    1m15.928s
user    0m5.965s
sys     0m0.239s
```

# Generated File
```
[bavaria@ip-172-31-57-130 hadoop-0.20-mapreduce]$ hdfs dfs -ls /user/bavaria/tgen512m
Found 9 items
-rw-r--r--   3 bavaria social          0 2016-11-18 10:20 /user/bavaria/tgen512m/_SUCCESS
-rw-r--r--   3 bavaria social  640000000 2016-11-18 10:20 /user/bavaria/tgen512m/part-m-00000
-rw-r--r--   3 bavaria social  640000000 2016-11-18 10:20 /user/bavaria/tgen512m/part-m-00001
-rw-r--r--   3 bavaria social  640000000 2016-11-18 10:20 /user/bavaria/tgen512m/part-m-00002
-rw-r--r--   3 bavaria social  640000000 2016-11-18 10:20 /user/bavaria/tgen512m/part-m-00003
-rw-r--r--   3 bavaria social  640000000 2016-11-18 10:20 /user/bavaria/tgen512m/part-m-00004
-rw-r--r--   3 bavaria social  640000000 2016-11-18 10:20 /user/bavaria/tgen512m/part-m-00005
-rw-r--r--   3 bavaria social  640000000 2016-11-18 10:20 /user/bavaria/tgen512m/part-m-00006
-rw-r--r--   3 bavaria social  640000000 2016-11-18 10:20 /user/bavaria/tgen512m/part-m-00007
```

# Number of Blocks
```
[bavaria@ip-172-31-57-130 hadoop-0.20-mapreduce]$ hdfs fsck /user/bavaria/tgen512m
Connecting to namenode via http://ip-172-31-57-130.ec2.internal:50070
FSCK started by bavaria (auth:SIMPLE) from /172.31.57.130 for path /user/bavaria/tgen512m at Fri Nov 18 10:22:50 UTC 2016
.........Status: HEALTHY
 Total size:    5120000000 B
 Total dirs:    1
 Total files:   9
 Total symlinks:                0
 Total blocks (validated):      312 (avg. block size 16410256 B)
 Minimally replicated blocks:   312 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
```

Important line is:  
**Total blocks (validated):      312 (avg. block size 16410256 B)**
