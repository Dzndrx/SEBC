[Dzndrx@ip-172-31-10-250 ~]$ time hadoop jar  /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 100000000 /user/Dzndrx/teragen
18/05/15 19:56:54 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-10-250.us-west-2.compute.internal/172.31.10.250:8032
18/05/15 19:56:55 INFO terasort.TeraGen: Generating 100000000 using 4
18/05/15 19:56:55 INFO mapreduce.JobSubmitter: number of splits:4
18/05/15 19:56:55 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
18/05/15 19:56:55 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
18/05/15 19:56:55 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526407739971_0004
18/05/15 19:56:55 INFO impl.YarnClientImpl: Submitted application application_1526407739971_0004
18/05/15 19:56:55 INFO mapreduce.Job: The url to track the job: http://ip-172-31-10-250.us-west-2.compute.internal:8088/proxy/application_1526407739971_0004/
18/05/15 19:56:55 INFO mapreduce.Job: Running job: job_1526407739971_0004
18/05/15 19:57:01 INFO mapreduce.Job: Job job_1526407739971_0004 running in uber mode : false
18/05/15 19:57:01 INFO mapreduce.Job:  map 0% reduce 0%
18/05/15 19:57:19 INFO mapreduce.Job:  map 19% reduce 0%
18/05/15 19:57:25 INFO mapreduce.Job:  map 27% reduce 0%
18/05/15 19:57:31 INFO mapreduce.Job:  map 31% reduce 0%
18/05/15 19:57:37 INFO mapreduce.Job:  map 39% reduce 0%
18/05/15 19:57:43 INFO mapreduce.Job:  map 48% reduce 0%
18/05/15 19:57:49 INFO mapreduce.Job:  map 53% reduce 0%
18/05/15 19:57:55 INFO mapreduce.Job:  map 58% reduce 0%
18/05/15 19:58:01 INFO mapreduce.Job:  map 71% reduce 0%
18/05/15 19:58:07 INFO mapreduce.Job:  map 75% reduce 0%
18/05/15 19:58:13 INFO mapreduce.Job:  map 78% reduce 0%
18/05/15 19:58:19 INFO mapreduce.Job:  map 90% reduce 0%
18/05/15 19:58:25 INFO mapreduce.Job:  map 95% reduce 0%
18/05/15 19:58:31 INFO mapreduce.Job:  map 98% reduce 0%
18/05/15 19:58:32 INFO mapreduce.Job:  map 99% reduce 0%
18/05/15 19:58:33 INFO mapreduce.Job:  map 100% reduce 0%
18/05/15 19:58:33 INFO mapreduce.Job: Job job_1526407739971_0004 completed successfully
18/05/15 19:58:33 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=605204
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=357607
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=357607
                Total vcore-milliseconds taken by all map tasks=357607
                Total megabyte-milliseconds taken by all map tasks=366189568
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1270
                CPU time spent (ms)=163340
                Physical memory (bytes) snapshot=780259328
                Virtual memory (bytes) snapshot=6349185024
                Total committed heap usage (bytes)=988282880
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000

real    1m41.716s
user    0m6.084s
sys     0m0.485s



###TERASORT
[Dzndrx@ip-172-31-10-250 ~]$ time hadoop jar  /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar \
> terasort -Dmapred.map.tasks=4 \
> /user/Dzndrx/teragen \
> /home/Dzndrx/terasort
18/05/15 20:00:36 INFO terasort.TeraSort: starting
18/05/15 20:00:38 INFO input.FileInputFormat: Total input paths to process : 4
Spent 232ms computing base-splits.
Spent 6ms computing TeraScheduler splits.
Computing input splits took 238ms
Sampling 10 splits of 300
Making 8 from 100000 sampled records
Computing parititions took 789ms
Spent 1030ms computing partitions.
18/05/15 20:00:39 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-10-250.us-west-2.compute.internal/172.31.10.250:8032
18/05/15 20:00:39 INFO mapreduce.JobSubmitter: number of splits:300
18/05/15 20:00:39 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
18/05/15 20:00:39 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526407739971_0005
18/05/15 20:00:39 INFO impl.YarnClientImpl: Submitted application application_1526407739971_0005
18/05/15 20:00:40 INFO mapreduce.Job: The url to track the job: http://ip-172-31-10-250.us-west-2.compute.internal:8088/proxy/application_1526407739971_0005/
18/05/15 20:00:40 INFO mapreduce.Job: Running job: job_1526407739971_0005
18/05/15 20:00:45 INFO mapreduce.Job: Job job_1526407739971_0005 running in uber mode : false
18/05/15 20:05:28 INFO mapreduce.Job: Job job_1526407739971_0005 completed successfully
18/05/15 20:05:28 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=4443326868
                FILE: Number of bytes written=8833303259
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000035100
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=924
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=300
                Launched reduce tasks=8
                Data-local map tasks=300
                Total time spent by all maps in occupied slots (ms)=2823742
                Total time spent by all reduces in occupied slots (ms)=625146
                Total time spent by all map tasks (ms)=2823742
                Total time spent by all reduce tasks (ms)=625146
                Total vcore-milliseconds taken by all map tasks=2823742
                Total vcore-milliseconds taken by all reduce tasks=625146
                Total megabyte-milliseconds taken by all map tasks=2891511808
                Total megabyte-milliseconds taken by all reduce tasks=640149504
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4342872473
                Input split bytes=35100
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4342872473
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =2400
                Failed Shuffles=0
                Merged Map outputs=2400
                GC time elapsed (ms)=47178
                CPU time spent (ms)=1399130
                Physical memory (bytes) snapshot=158728884224
                Virtual memory (bytes) snapshot=488362528768
                Total committed heap usage (bytes)=181496446976
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10000000000
        File Output Format Counters
                Bytes Written=10000000000
18/05/15 20:05:28 INFO terasort.TeraSort: done

real    4m53.173s
user    0m8.641s
sys     0m0.597s