# Repo
```
[centos@ip-172-31-57-130 ~]$ ls /etc/yum.repos.d
CentOS-Base.repo  CentOS-Debuginfo.repo  CentOS-Media.repo    CentOS-Vault.repo      mysql-community.repo
CentOS-CR.repo    CentOS-fasttrack.repo  CentOS-Sources.repo  cloudera-manager.repo  mysql-community-source.repo
```

# Redefine Grant for scm User
> mysql> grant all on cms.* to 'cms'@'ip-172-31-57-131.ec2.internal';  
> Query OK, 0 rows affected (0.01 sec)  

```
mysql> show grants for cms@'ip-172-31-57-131.ec2.internal';
+--------------------------------------------------------------------------+
| Grants for cms@ip-172-31-57-130.ec2.internal                             |
+--------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'cms'@'ip-172-31-57-131.ec2.internal'              |
| GRANT ALL PRIVILEGES ON `cms`.* TO 'cms'@'ip-172-31-57-131.ec2.internal' |
+--------------------------------------------------------------------------+
2 rows in set (0.00 sec)

mysql> show grants for cms;
ERROR 1141 (42000): There is no such grant defined for user 'cms' on host '%'
```

# Prepare DB
```
[centos@ip-172-31-57-130 schema]$ sudo ./scm_prepare_database.sh mysql -h ip-172-31-57-131.ec2.internal scm scm password
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!
```