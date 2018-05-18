```
[root@ip-172-31-2-224 centos]# hostname -f
ip-172-31-2-224.us-west-2.compute.internal
[root@ip-172-31-2-224 centos]# mysql -u scmadmin -p -e "status;"
Enter password:
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          15
Current database:
Current user:           scmadmin@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.56-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 10 min 54 sec

Threads: 1  Questions: 51  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.077
--------------

[root@ip-172-31-2-224 centos]# mysql -u scmadmin -p -e "show databases;"
Enter password:
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| oozie              |
| rman               |
| scm                |
| sentry             |
+--------------------+
```