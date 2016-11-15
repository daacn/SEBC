# Prepare File
> hadoop fs -mkdir precious  
> hadoop fs -put very-valueable precious/  
  
# Enable/create Snapshot
> hdfs dfsadmin -allowSnapshot /user/daniel/precious (as user hdfs)  
> hdfs dfs -createSnapshot /user/daniel/precious sebc-hdfs-test  

# Delete precious information
> hadoop fs -rm -r precious  
> rm: Failed to move to trash: hdfs://ip-172-31-50-73.ec2.internal:8020/user/daniel/precious: The directory /user/daniel/precious cannot be deleted since /user/daniel/precious is snapshottable and already has snapshots  
>   
> hadoop fs -rm precious/very-valueable  

# Recover
> hadoop fs -cp precious/.snapshot/sebc-hdfs-test/very-valueable precious/very-valueable
