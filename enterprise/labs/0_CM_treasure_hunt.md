# What is ubertask optimization?
Running multiple "small" jobs sequentially in the same JVM  
  
# Where in CM is the Kerberos Security Realm value displayed?
It's can be found under Administration -> Settings  -> security_realm  
  
# Which CDH service(s) host a property for enabling Kerberos authentication?
All (at least all installed services in my installation)
  
# How do you upgrade the CM agents?
Manually on OS/package level (yum upgrade ...) or during/within upgrading the CM Server  
  
# Give the tsquery statement used to chart Hue's CPU utilization?
select cpu_user_rate / getHostFact(numCores, 1) * 100, cpu_system_rate / getHostFact(numCores, 1) * 100 where entityName=$ROLENAME  
  
# Name all the roles that make up the Hive service
Gateway, Hive Metastore Server, HiveServer2  
  
# What steps must be completed before integrating Cloudera Manager with Kerberos?
* Set up a working KDC. Cloudera Manager supports MIT KDC and Active Directory.  
* The KDC should be configured to have non-zero ticket lifetime and renewal lifetime. CDH will not work properly if tickets are not renewable.  
* OpenLdap client libraries should be installed on the Cloudera Manager Server host if you want to use Active Directory. Also, Kerberos client libraries should be installed on ALL hosts.  
* Cloudera Manager needs an account that has permissions to create other accounts in the KDC.  