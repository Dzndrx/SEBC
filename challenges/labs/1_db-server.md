[root@ip-172-31-6-237 centos]# hostname -f
ip-172-31-6-237.us-west-2.compute.internal
[root@ip-172-31-6-237 centos]# mysql -u dbadmin -p elabrigo -e "status;"
Enter password:
ERROR 1044 (42000): Access denied for user 'dbadmin'@'%' to database 'elabrigo'
[root@ip-172-31-6-237 centos]# mysql -u root -p -e "status;"
Enter password:
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          13
Current database:
Current user:           root@localhost
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
Uptime:                 23 min 23 sec

Threads: 1  Questions: 47  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.033
--------------

[root@ip-172-31-6-237 centos]# mysql -u root -p -e "show databases;"
Enter password:
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
