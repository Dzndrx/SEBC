[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfs -mkdir precious
[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfs -put /home/Dzndrx/SEBC.zip /user/Dzndrx/precious
[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfs -ls /user/Dzndrx
Found 3 items
drwx------   - Dzndrx supergroup          0 2018-05-15 20:05 /user/Dzndrx/.staging
drwxr-xr-x   - Dzndrx supergroup          0 2018-05-16 03:20 /user/Dzndrx/precious
drwxr-xr-x   - Dzndrx supergroup          0 2018-05-15 19:58 /user/Dzndrx/teragen
[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfs -ls /user/Dzndrx/precious
Found 1 items
-rw-r--r--   3 Dzndrx supergroup     471851 2018-05-16 03:20 /user/Dzndrx/precious/SEBC.zip
[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfsadmin -allowSnapshot /user/Dzndrx/precious
Allowing snaphot on /user/Dzndrx/precious succeeded
[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfs -createSnapshot /user/Dzndrx/precious sebc-hdfs-test
Created snapshot /user/Dzndrx/precious/.snapshot/sebc-hdfs-test
[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfs -rm -r -skipTrash /user/Dzndrx/precious/
rm: The directory /user/Dzndrx/precious cannot be deleted since /user/Dzndrx/precious is snapshottable and already has snapshots
[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfs -rm -r -skipTrash /user/Dzndrx/precious/SEBC.zip
Deleted /user/Dzndrx/precious/SEBC.zip
[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfs -ls /user/Dzndrx/precious/.snapshot
Found 1 items
drwxr-xr-x   - Dzndrx supergroup          0 2018-05-16 03:26 /user/Dzndrx/precious/.snapshot/sebc-hdfs-test
[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfs -cat /user/Dzndrx/precious/.snapshot/sebc-hdfs-test
cat: `/user/Dzndrx/precious/.snapshot/sebc-hdfs-test': Is a directory
[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfs -ls /user/Dzndrx/precious/.snapshot/sebc-hdfs-test
Found 1 items
-rw-r--r--   3 Dzndrx supergroup     471851 2018-05-16 03:20 /user/Dzndrx/precious/.snapshot/sebc-hdfs-test/SEBC.zip
[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfs -cp /user/Dzndrx/precious/.snapshot/sebc-hdfs-test/SEBC.zip /user/Dzndrx/precious
[Dzndrx@ip-172-31-10-250 centos]$ hdfs dfs -ls /user/Dzndrx/precious
Found 1 items
-rw-r--r--   3 Dzndrx supergroup     471851 2018-05-16 03:34 /user/Dzndrx/precious/SEBC.zip