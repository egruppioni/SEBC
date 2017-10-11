```
[root@ip-172-31-26-219 ~]# kinit egruppioni
Password for egruppioni@EGRUPPIONI.HQ:
[root@ip-172-31-26-219 ~]# beeline
Beeline version 1.1.0-cdh5.12.1 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-18-42.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-18-42.eu-central-1.compute.internal@EGRUPPIONI.HQ
scan complete in 2ms
Connecting to jdbc:hive2://ip-172-31-18-42.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-18-42.eu-central-1.compute.internal@EGRUPPIONI.HQ
Connected to: Apache Hive (version 1.1.0-cdh5.12.1)
Driver: Hive JDBC (version 1.1.0-cdh5.12.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> show tables;
INFO  : Compiling command(queryId=hive_20171011051515_5cc52e50-19bc-4100-ac32-2ca4b848a555): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171011051515_5cc52e50-19bc-4100-ac32-2ca4b848a555); Time taken: 0.794 seconds
INFO  : Executing command(queryId=hive_20171011051515_5cc52e50-19bc-4100-ac32-2ca4b848a555): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011051515_5cc52e50-19bc-4100-ac32-2ca4b848a555); Time taken: 0.369 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.591 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.>  GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20171011053232_8dda6ecb-09bb-44e9-8d71-e54e855e386d): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053232_8dda6ecb-09bb-44e9-8d71-e54e855e386d); Time taken: 0.105 seconds
INFO  : Executing command(queryId=hive_20171011053232_8dda6ecb-09bb-44e9-8d71-e54e855e386d): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
ERROR : Error processing Sentry command: Role: sentry_admin doesn't exist..
ERROR : FAILED: Execution Error, return code 1 from org.apache.hadoop.hive.ql.exec.SentryGrantRevokeTask. SentryNoSuchObjectException: Role: sentry_admin doesn't exist.
INFO  : Completed executing command(queryId=hive_20171011053232_8dda6ecb-09bb-44e9-8d71-e54e855e386d); Time taken: 0.515 seconds
Error: Error while processing statement: FAILED: Execution Error, return code 1 from org.apache.hadoop.hive.ql.exec.SentryGrantRevokeTask. SentryNoSuchObjectException: Role: sentry_admin doesn't exist. (state=08S01,code=1)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20171011053333_4700b5a4-0685-425c-a068-4bea7c00d2d5): CREATE ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053333_4700b5a4-0685-425c-a068-4bea7c00d2d5); Time taken: 0.102 seconds
INFO  : Executing command(queryId=hive_20171011053333_4700b5a4-0685-425c-a068-4bea7c00d2d5): CREATE ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053333_4700b5a4-0685-425c-a068-4bea7c00d2d5); Time taken: 0.112 seconds
INFO  : OK
No rows affected (0.23 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20171011053333_3aa767d6-2407-4733-896c-df3b754d864b): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053333_3aa767d6-2407-4733-896c-df3b754d864b); Time taken: 0.072 seconds
INFO  : Executing command(queryId=hive_20171011053333_3aa767d6-2407-4733-896c-df3b754d864b): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053333_3aa767d6-2407-4733-896c-df3b754d864b); Time taken: 0.051 seconds
INFO  : OK
No rows affected (0.138 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> GRANT ROLE sentry_admin TO GROUP egruppioni;
INFO  : Compiling command(queryId=hive_20171011053333_74731827-d491-465b-8fa6-01589b8699ba): GRANT ROLE sentry_admin TO GROUP egruppioni
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053333_74731827-d491-465b-8fa6-01589b8699ba); Time taken: 0.069 seconds
INFO  : Executing command(queryId=hive_20171011053333_74731827-d491-465b-8fa6-01589b8699ba): GRANT ROLE sentry_admin TO GROUP egruppioni
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053333_74731827-d491-465b-8fa6-01589b8699ba); Time taken: 0.073 seconds
INFO  : OK
No rows affected (0.156 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171011053333_6626e6cd-0e67-4924-babd-3367975a07d5): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053333_6626e6cd-0e67-4924-babd-3367975a07d5); Time taken: 0.081 seconds
INFO  : Executing command(queryId=hive_20171011053333_6626e6cd-0e67-4924-babd-3367975a07d5): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053333_6626e6cd-0e67-4924-babd-3367975a07d5); Time taken: 0.15 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.296 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> !quit
Closing: 0: jdbc:hive2://ip-172-31-18-42.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-18-42.eu-central-1.compute.internal@EGRUPPIONI.HQ
[root@ip-172-31-26-219 ~]# groupadd selector
[root@ip-172-31-26-219 ~]# groupadd inserters
[root@ip-172-31-26-219 ~]# useradd -u 1100 -g selector george
[root@ip-172-31-26-219 ~]# useradd -u 1200 -g inserters ferdinand
[root@ip-172-31-26-219 ~]# beeline
Beeline version 1.1.0-cdh5.12.1 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-18-42.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-18-42.eu-central-1.compute.internal@EGRUPPIONI.HQ
scan complete in 2ms
Connecting to jdbc:hive2://ip-172-31-18-42.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-18-42.eu-central-1.compute.internal@EGRUPPIONI.HQ
Connected to: Apache Hive (version 1.1.0-cdh5.12.1)
Driver: Hive JDBC (version 1.1.0-cdh5.12.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> CREATE ROLE reads;
INFO  : Compiling command(queryId=hive_20171011053636_760867b3-0baf-4f7a-903a-c82b1a7614ff): CREATE ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053636_760867b3-0baf-4f7a-903a-c82b1a7614ff); Time taken: 0.069 seconds
INFO  : Executing command(queryId=hive_20171011053636_760867b3-0baf-4f7a-903a-c82b1a7614ff): CREATE ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053636_760867b3-0baf-4f7a-903a-c82b1a7614ff); Time taken: 0.037 seconds
INFO  : OK
No rows affected (0.174 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> CREATE ROLE writes;
INFO  : Compiling command(queryId=hive_20171011053737_ce2c72ab-1126-4306-a17e-fcf9b138cd46): CREATE ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053737_ce2c72ab-1126-4306-a17e-fcf9b138cd46); Time taken: 0.065 seconds
INFO  : Executing command(queryId=hive_20171011053737_ce2c72ab-1126-4306-a17e-fcf9b138cd46): CREATE ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053737_ce2c72ab-1126-4306-a17e-fcf9b138cd46); Time taken: 0.025 seconds
INFO  : OK
No rows affected (0.105 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> GRANT SELECT ON DATABASE default TO ROLE reads;
INFO  : Compiling command(queryId=hive_20171011053737_89a3f50d-52bd-4b1c-9f9c-d83aad21e45c): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053737_89a3f50d-52bd-4b1c-9f9c-d83aad21e45c); Time taken: 0.068 seconds
INFO  : Executing command(queryId=hive_20171011053737_89a3f50d-52bd-4b1c-9f9c-d83aad21e45c): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053737_89a3f50d-52bd-4b1c-9f9c-d83aad21e45c); Time taken: 0.03 seconds
INFO  : OK
No rows affected (0.118 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> GRANT ROLE reads TO GROUP selector;
INFO  : Compiling command(queryId=hive_20171011053737_f37bf3d8-63ea-4a1a-9242-a17ea2512891): GRANT ROLE reads TO GROUP selector
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053737_f37bf3d8-63ea-4a1a-9242-a17ea2512891); Time taken: 0.072 seconds
INFO  : Executing command(queryId=hive_20171011053737_f37bf3d8-63ea-4a1a-9242-a17ea2512891): GRANT ROLE reads TO GROUP selector
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053737_f37bf3d8-63ea-4a1a-9242-a17ea2512891); Time taken: 0.029 seconds
INFO  : OK
No rows affected (0.116 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> REVOKE ALL ON DATABASE default FROM ROLE writes;
INFO  : Compiling command(queryId=hive_20171011053737_3eeef3f2-a149-43d5-a767-a2b86dacf7ca): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053737_3eeef3f2-a149-43d5-a767-a2b86dacf7ca); Time taken: 0.066 seconds
INFO  : Executing command(queryId=hive_20171011053737_3eeef3f2-a149-43d5-a767-a2b86dacf7ca): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053737_3eeef3f2-a149-43d5-a767-a2b86dacf7ca); Time taken: 0.079 seconds
INFO  : OK
No rows affected (0.171 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> GRANT SELECT ON default.sample_07 TO ROLE writes;
INFO  : Compiling command(queryId=hive_20171011053737_1c26de69-6c7b-4032-b7db-ff62d916ac8c): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053737_1c26de69-6c7b-4032-b7db-ff62d916ac8c); Time taken: 0.067 seconds
INFO  : Executing command(queryId=hive_20171011053737_1c26de69-6c7b-4032-b7db-ff62d916ac8c): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053737_1c26de69-6c7b-4032-b7db-ff62d916ac8c); Time taken: 0.035 seconds
INFO  : OK
No rows affected (0.118 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> GRANT ROLE writes TO GROUP inserters;
INFO  : Compiling command(queryId=hive_20171011053737_e4925b2d-d738-423a-8f51-dd7636b1039b): GRANT ROLE writes TO GROUP inserters
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053737_e4925b2d-d738-423a-8f51-dd7636b1039b); Time taken: 0.078 seconds
INFO  : Executing command(queryId=hive_20171011053737_e4925b2d-d738-423a-8f51-dd7636b1039b): GRANT ROLE writes TO GROUP inserters
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053737_e4925b2d-d738-423a-8f51-dd7636b1039b); Time taken: 0.05 seconds
INFO  : OK
No rows affected (0.144 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.>


[root@ip-172-31-30-118 ~]# kinit george
Password for george@EGRUPPIONI.HQ:
[root@ip-172-31-30-118 ~]# beeline
Beeline version 1.1.0-cdh5.12.1 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-18-42.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-18-42.eu-central-1.compute.internal@EGRUPPIONI.HQ
scan complete in 2ms
Connecting to jdbc:hive2://ip-172-31-18-42.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-18-42.eu-central-1.compute.internal@EGRUPPIONI.HQ
Connected to: Apache Hive (version 1.1.0-cdh5.12.1)
Driver: Hive JDBC (version 1.1.0-cdh5.12.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> show tables;
INFO  : Compiling command(queryId=hive_20171011053838_713daa6f-89f2-41ba-8bd0-646c6223dc15): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053838_713daa6f-89f2-41ba-8bd0-646c6223dc15); Time taken: 0.075 seconds
INFO  : Executing command(queryId=hive_20171011053838_713daa6f-89f2-41ba-8bd0-646c6223dc15): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053838_713daa6f-89f2-41ba-8bd0-646c6223dc15); Time taken: 1.567 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (1.741 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.>


[root@ip-172-31-20-187 ~]# kinit ferdinand
Password for ferdinand@EGRUPPIONI.HQ:
[root@ip-172-31-20-187 ~]# beeline
Beeline version 1.1.0-cdh5.12.1 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-18-42.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-18-42.eu-central-1.compute.internal@EGRUPPIONI.HQ
scan complete in 3ms
Connecting to jdbc:hive2://ip-172-31-18-42.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-18-42.eu-central-1.compute.internal@EGRUPPIONI.HQ
Connected to: Apache Hive (version 1.1.0-cdh5.12.1)
Driver: Hive JDBC (version 1.1.0-cdh5.12.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.> show tables;
INFO  : Compiling command(queryId=hive_20171011053939_248eb539-f26d-4aaa-bfab-bb3f4ab681b5): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171011053939_248eb539-f26d-4aaa-bfab-bb3f4ab681b5); Time taken: 0.074 seconds
INFO  : Executing command(queryId=hive_20171011053939_248eb539-f26d-4aaa-bfab-bb3f4ab681b5): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171011053939_248eb539-f26d-4aaa-bfab-bb3f4ab681b5); Time taken: 0.149 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.325 seconds)
0: jdbc:hive2://ip-172-31-18-42.eu-central-1.>

```