# Before setting Authorizations

```
0: jdbc:hive2://localhost:10000/default> show tables;
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.452 seconds)
```

# After creating sentry_admin group
```
0: jdbc:hive2://localhost:10000/default> show tables;
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
```

# Setting up Authorizations
See Lab description.  

# Test with George
```
0: jdbc:hive2://localhost:10000/default> show tables;
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
```

# Test with Ferdinand
```
0: jdbc:hive2://localhost:10000/default> show tables;
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.318 seconds)
```