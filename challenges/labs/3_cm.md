# MySQL Grants
```
mysql> show grants for rman;
+-----------------------------------------------------------------------------------------------------+
| Grants for rman@%                                                                                   |
+-----------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'rman'@'%' IDENTIFIED BY PASSWORD '*2470C0C06DEE42FD1618BB99005ADCA2EC9D1E19' |
| GRANT ALL PRIVILEGES ON `rman`.* TO 'rman'@'%'                                                      |
+-----------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)

mysql> show grants for hive;
+-----------------------------------------------------------------------------------------------------+
| Grants for hive@%                                                                                   |
+-----------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'hive'@'%' IDENTIFIED BY PASSWORD '*2470C0C06DEE42FD1618BB99005ADCA2EC9D1E19' |
| GRANT ALL PRIVILEGES ON `hive`.* TO 'hive'@'%'                                                      |
+-----------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)

mysql> show grants for scm;
+----------------------------------------------------------------------------------------------------+
| Grants for scm@%                                                                                   |
+----------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'scm'@'%' IDENTIFIED BY PASSWORD '*2470C0C06DEE42FD1618BB99005ADCA2EC9D1E19' |
| GRANT ALL PRIVILEGES ON `scm`.* TO 'scm'@'%'                                                       |
+----------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)
```

# New User Dirs:
```
[bavaria@ip-172-31-57-130 cloudera-scm-server]$ hadoop fs -ls /user
Found 6 items
drwxr-xr-x   - bavaria social              0 2016-11-18 10:02 /user/bavaria
drwxrwxrwx   - mapred  hadoop              0 2016-11-18 09:49 /user/history
drwxrwxr-t   - hive    hive                0 2016-11-18 09:50 /user/hive
drwxrwxr-x   - hue     hue                 0 2016-11-18 09:50 /user/hue
drwxrwxr-x   - oozie   oozie               0 2016-11-18 09:51 /user/oozie
drwxr-xr-x   - saxony  democratic          0 2016-11-18 10:02 /user/saxony
```

# Hosts through API
```JSON
{
items: [
{
hostId: "i-fc2262f2",
ipAddress: "172.31.57.130",
hostname: "ip-172-31-57-130.ec2.internal",
rackId: "/default",
hostUrl: "http://ip-172-31-57-130.ec2.internal:7180/cmf/hostRedirect/i-fc2262f2",
maintenanceMode: false,
maintenanceOwners: [ ],
commissionState: "COMMISSIONED",
numCores: 4,
numPhysicalCores: 2,
totalPhysMemBytes: 15332438016
},
{
hostId: "i-f32262fd",
ipAddress: "172.31.57.131",
hostname: "ip-172-31-57-131.ec2.internal",
rackId: "/default",
hostUrl: "http://ip-172-31-57-130.ec2.internal:7180/cmf/hostRedirect/i-f32262fd",
maintenanceMode: false,
maintenanceOwners: [ ],
commissionState: "COMMISSIONED",
numCores: 4,
numPhysicalCores: 2,
totalPhysMemBytes: 15332438016
},
{
hostId: "i-f22262fc",
ipAddress: "172.31.57.132",
hostname: "ip-172-31-57-132.ec2.internal",
rackId: "/default",
hostUrl: "http://ip-172-31-57-130.ec2.internal:7180/cmf/hostRedirect/i-f22262fc",
maintenanceMode: false,
maintenanceOwners: [ ],
commissionState: "COMMISSIONED",
numCores: 4,
numPhysicalCores: 2,
totalPhysMemBytes: 15332438016
},
{
hostId: "i-f12262ff",
ipAddress: "172.31.57.133",
hostname: "ip-172-31-57-133.ec2.internal",
rackId: "/default",
hostUrl: "http://ip-172-31-57-130.ec2.internal:7180/cmf/hostRedirect/i-f12262ff",
maintenanceMode: false,
maintenanceOwners: [ ],
commissionState: "COMMISSIONED",
numCores: 4,
numPhysicalCores: 2,
totalPhysMemBytes: 15332438016
},
{
hostId: "i-f02262fe",
ipAddress: "172.31.57.134",
hostname: "ip-172-31-57-134.ec2.internal",
rackId: "/default",
hostUrl: "http://ip-172-31-57-130.ec2.internal:7180/cmf/hostRedirect/i-f02262fe",
maintenanceMode: false,
maintenanceOwners: [ ],
commissionState: "COMMISSIONED",
numCores: 4,
numPhysicalCores: 2,
totalPhysMemBytes: 15332438016
}
]
}
```