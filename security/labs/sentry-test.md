# Verify user privileges

```
Vbeeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-10-250.us-west-2.com                                                                    pute.internal@EXAMPLE.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-10-250.us-west-2.compute                                                                    .internal@EXAMPLE.COM
Connected to: Apache Hive (version 1.1.0-cdh5.14.2)
Driver: Hive JDBC (version 1.1.0-cdh5.14.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20180516145050_aa978340-2317-449b-b5c4-38929d2d259c): show ta                                                                    bles
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:                                                                    from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20180516145050_aa978340-2317-449b-b5c4-38929d2d259c                                                                    ); Time taken: 0.115 seconds
INFO  : Executing command(queryId=hive_20180516145050_aa978340-2317-449b-b5c4-38929d2d259c): show ta                                                                    bles
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180516145050_aa978340-2317-449b-b5c4-38929d2d259c                                                                    ); Time taken: 0.144 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (0.364 seconds)
```

# Create a Sentry role with full authorization

```
0: jdbc:hive2://localhost:10000/default> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20180516145050_bda21f14-1814-4f15-bd04-c36dfd9ca8f1): CREATE                                                                     ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180516145050_bda21f14-1814-4f15-bd04-c36dfd9ca8f1                                                                    ); Time taken: 0.073 seconds
INFO  : Executing command(queryId=hive_20180516145050_bda21f14-1814-4f15-bd04-c36dfd9ca8f1): CREATE                                                                     ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180516145050_bda21f14-1814-4f15-bd04-c36dfd9ca8f1                                                                    ); Time taken: 0.078 seconds
INFO  : OK
No rows affected (0.165 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20180516145151_9759f815-a10c-4fa7-bdde-699a734d2304): GRANT A                                                                    LL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180516145151_9759f815-a10c-4fa7-bdde-699a734d2304                                                                    ); Time taken: 0.081 seconds
INFO  : Executing command(queryId=hive_20180516145151_9759f815-a10c-4fa7-bdde-699a734d2304): GRANT A                                                                    LL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180516145151_9759f815-a10c-4fa7-bdde-699a734d2304                                                                    ); Time taken: 0.027 seconds
INFO  : OK
No rows affected (0.125 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT ROLE sentry_admin TO GROUP stest;
INFO  : Compiling command(queryId=hive_20180516145151_466a4ecb-3946-405b-9b15-5272a2fc75ee): GRANT R                                                                    OLE sentry_admin TO GROUP stest
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180516145151_466a4ecb-3946-405b-9b15-5272a2fc75ee                                                                    ); Time taken: 0.071 seconds
INFO  : Executing command(queryId=hive_20180516145151_466a4ecb-3946-405b-9b15-5272a2fc75ee): GRANT R                                                                    OLE sentry_admin TO GROUP stest
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180516145151_466a4ecb-3946-405b-9b15-5272a2fc75ee                                                                    ); Time taken: 0.052 seconds
INFO  : OK
No rows affected (0.138 seconds)
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20180516145252_7bab545a-19a0-42f7-9e9f-209c99ba6da8): show ta                                                                    bles
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:                                                                    from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20180516145252_7bab545a-19a0-42f7-9e9f-209c99ba6da8                                                                    ); Time taken: 0.066 seconds
INFO  : Executing command(queryId=hive_20180516145252_7bab545a-19a0-42f7-9e9f-209c99ba6da8): show ta                                                                    bles
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180516145252_7bab545a-19a0-42f7-9e9f-209c99ba6da8                                                                    ); Time taken: 0.132 seconds
INFO  : OK
+-------------------+--+
|     tab_name      |
+-------------------+--+
| 201402_trip_data  |
| sample            |
+-------------------+--+
2 rows selected (0.261 seconds)
```

# kinit as george, then login to beeline also ferdinand

```
[root@ip-172-31-10-250 centos]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: george@EXAMPLE.COM

Valid starting       Expires              Service principal
05/16/2018 15:06:52  05/17/2018 15:06:52  krbtgt/EXAMPLE.COM@EXAMPLE.COM
        renew until 05/23/2018 15:06:52
[root@ip-172-31-10-250 centos]# beeline
Beeline version 1.1.0-cdh5.14.2 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-10-250.us-west-2.com                                                                    pute.internal@EXAMPLE.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-10-250.us-west-2.compute                                                                    .internal@EXAMPLE.COM
Connected to: Apache Hive (version 1.1.0-cdh5.14.2)
Driver: Hive JDBC (version 1.1.0-cdh5.14.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20180516150707_773dea19-2b63-4782-91a9-9c5de11d83e0): show ta                                                                    bles
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:                                                                    from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20180516150707_773dea19-2b63-4782-91a9-9c5de11d83e0                                                                    ); Time taken: 0.075 seconds
INFO  : Executing command(queryId=hive_20180516150707_773dea19-2b63-4782-91a9-9c5de11d83e0): show ta                                                                    bles
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180516150707_773dea19-2b63-4782-91a9-9c5de11d83e0                                                                    ); Time taken: 0.112 seconds
INFO  : OK
+-------------------+--+
|     tab_name      |
+-------------------+--+
| 201402_trip_data  |
| sample            |
+-------------------+--+



[root@ip-172-31-10-250 centos]# beeline
Beeline version 1.1.0-cdh5.14.2 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-10-250.us-west-2.compute.internal@EXAMPLE.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-10-250.us-west-2.compute.internal@EXAMPLE.COM
Connected to: Apache Hive (version 1.1.0-cdh5.14.2)
Driver: Hive JDBC (version 1.1.0-cdh5.14.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20180516150808_42822a12-46b7-40ad-9519-e2dee4f3ed21): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20180516150808_42822a12-46b7-40ad-9519-e2dee4f3ed21); Time taken: 0.078 seconds
INFO  : Executing command(queryId=hive_20180516150808_42822a12-46b7-40ad-9519-e2dee4f3ed21): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180516150808_42822a12-46b7-40ad-9519-e2dee4f3ed21); Time taken: 0.135 seconds
INFO  : OK
+-------------------+--+
|     tab_name      |
+-------------------+--+
| 201402_trip_data  |
+-------------------+--+
1 row selected (0.336 seconds)
0: jdbc:hive2://localhost:10000/default>
```