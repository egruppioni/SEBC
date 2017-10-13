```

[root@ip-172-31-4-206 yum.repos.d]# hostname -f
ip-172-31-4-206.eu-central-1.compute.internal
[root@ip-172-31-4-206 yum.repos.d]# mysql -u root -pbitbang -e "status;"
--------------
mysql  Ver 14.14 Distrib 5.5.57, for Linux (x86_64) using readline 5.1

Connection id:          11
Current database:
Current user:           root@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server version:         5.5.57-log MySQL Community Server (GPL)
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 2 min 44 sec

Threads: 1  Questions: 44  Slow queries: 0  Opens: 34  Flush tables: 1  Open tables: 27  Queries per second avg: 0.268
--------------

[root@ip-172-31-4-206 ~]#  mysql -u root -pbitbang -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+

```