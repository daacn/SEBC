# Installation (MariaDB Master and Slave)
> sudo yum install mariadb-server  
> sudo systemctl enable mariadb  
> sudo systemctl start mariadb  
>   
> sudo /usr/bin/mysql_secure_installation: ...  

# Install JDBC (all nodes):
> wget http://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.40.tar.gz  
> tar -xzvf mysql-connector-java-5.1.40.tar.gz  
> sudo mkdir /usr/share/java  
> sudo mv mysql-connector-java-5.1.40/mysql-connector-java-5.1.40-bin.jar /usr/share/java/mysql-connector-java.jar   
> echo "PATH=/usr/share/java/:$PATH" >> ~/.bashrc  
> source ~/.bashrc  

# Setup replication
## On Master
Update configuration (/etc/my.cnf.d/server.cnf), section [mariadb]:
> bind-address = 0.0.0.0  
> log-bin  
> server_id=1  
> log-basename=master1  
  
Restart MariaDB, then in SQL:  
> GRANT REPLICATION SLAVE ON *.* TO 'replication_user' IDENTIFIED BY 'password';  
> SET GLOBAL binlog_format = 'ROW';  
> FLUSH TABLES WITH READ LOCK;  

## On Slave
Update configuration (/etc/my.cnf.d/server.cnf), section [mariadb]:
> bind-address = 0.0.0.0  
> server_id=2   
  
Restart MariaDB, then in SQL:  
> CHANGE MASTER TO  
>   MASTER_HOST='ip-172-31-50-73.ec2.internal',  
>   MASTER_USER='replication_user',  
>   MASTER_PASSWORD='password',  
>   MASTER_LOG_FILE='master1-bin.000004',  
>   MASTER_LOG_POS=395,  
>   MASTER_CONNECT_RETRY=10;  
>   
> START SLAVE;
>   
> SHOW SLAVE STATUS \G;  
*************************** 1. row ***************************  
               Slave_IO_State: Waiting for master to send event  
                  Master_Host: ip-172-31-50-73.ec2.internal  
                  Master_User: replication_user  
                  Master_Port: 3306  
                Connect_Retry: 10  
              Master_Log_File: master1-bin.000004  
          Read_Master_Log_Pos: 31657908  
               Relay_Log_File: mariadb-relay-bin.000002  
                Relay_Log_Pos: 31658044  
        Relay_Master_Log_File: master1-bin.000004  
             Slave_IO_Running: Yes  
            Slave_SQL_Running: Yes  
              Replicate_Do_DB:  
          Replicate_Ignore_DB:  
           Replicate_Do_Table:  
       Replicate_Ignore_Table:  
      Replicate_Wild_Do_Table:  
  Replicate_Wild_Ignore_Table:  
                   Last_Errno: 0  
                   Last_Error:  
                 Skip_Counter: 0  
          Exec_Master_Log_Pos: 31657908  
              Relay_Log_Space: 31658340  
              Until_Condition: None  
               Until_Log_File:  
                Until_Log_Pos: 0  
           Master_SSL_Allowed: No  
           Master_SSL_CA_File:  
           Master_SSL_CA_Path:  
              Master_SSL_Cert:  
            Master_SSL_Cipher:  
               Master_SSL_Key:  
        Seconds_Behind_Master: 0  
Master_SSL_Verify_Server_Cert: No  
                Last_IO_Errno: 0  
                Last_IO_Error:  
               Last_SQL_Errno: 0  
               Last_SQL_Error:  
  Replicate_Ignore_Server_Ids:  
             Master_Server_Id: 1  

             
# Prepare Databases for CM installation
> create database cmf DEFAULT CHARACTER SET utf8;  
> grant all on cmf.* to 'cmf'@'%' identified by 'password';  

> sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql cmf cmf password  
