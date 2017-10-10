```
[root@ip-172-31-26-219 ~]# useradd egruppioni

[root@ip-172-31-26-219 ~]# sudo -u hdfs  hdfs dfs -mkdir -p /user/egruppioni
[root@ip-172-31-26-219 ~]# sudo -u hdfs  hdfs dfs -chown -R 

[root@ip-172-31-26-219 ~]# sudo su egruppioni
[egruppioni@ip-172-31-26-219 root]$ time hadoop jar /opt/cloudera/parcels/CDH/ja                                                                                                                               rs/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 10                                                                                                                               7374182 teragen
17/10/10 08:25:46 INFO client.RMProxy: Connecting to ResourceManager at ip-172-3                                                                                                                               1-18-42.eu-central-1.compute.internal/172.31.18.42:8032
17/10/10 08:25:46 INFO terasort.TeraGen: Generating 107374182 using 4
17/10/10 08:25:46 INFO mapreduce.JobSubmitter: number of splits:4
17/10/10 08:25:46 INFO Configuration.deprecation: mapred.map.tasks is deprecated                                                                                                                               . Instead, use mapreduce.job.maps
17/10/10 08:25:46 INFO Configuration.deprecation: dfs.block.size is deprecated.                                                                                                                                Instead, use dfs.blocksize
17/10/10 08:25:47 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_15                                                                                                                               07634065337_0001
17/10/10 08:25:47 INFO impl.YarnClientImpl: Submitted application application_15                                                                                                                               07634065337_0001
17/10/10 08:25:47 INFO mapreduce.Job: The url to track the job: http://ip-172-31                                                                                                                               -18-42.eu-central-1.compute.internal:8088/proxy/application_1507634065337_0001/
17/10/10 08:25:47 INFO mapreduce.Job: Running job: job_1507634065337_0001
17/10/10 08:25:54 INFO mapreduce.Job: Job job_1507634065337_0001 running in uber                                                                                                                                mode : false
17/10/10 08:25:54 INFO mapreduce.Job:  map 0% reduce 0%
17/10/10 08:26:12 INFO mapreduce.Job:  map 8% reduce 0%
17/10/10 08:26:17 INFO mapreduce.Job:  map 17% reduce 0%
17/10/10 08:26:18 INFO mapreduce.Job:  map 20% reduce 0%
17/10/10 08:26:23 INFO mapreduce.Job:  map 24% reduce 0%
17/10/10 08:26:24 INFO mapreduce.Job:  map 26% reduce 0%
17/10/10 08:26:29 INFO mapreduce.Job:  map 27% reduce 0%
17/10/10 08:26:34 INFO mapreduce.Job:  map 28% reduce 0%
17/10/10 08:26:35 INFO mapreduce.Job:  map 29% reduce 0%
17/10/10 08:26:36 INFO mapreduce.Job:  map 30% reduce 0%
17/10/10 08:26:42 INFO mapreduce.Job:  map 33% reduce 0%
17/10/10 08:26:43 INFO mapreduce.Job:  map 34% reduce 0%
17/10/10 08:26:47 INFO mapreduce.Job:  map 36% reduce 0%
17/10/10 08:26:49 INFO mapreduce.Job:  map 37% reduce 0%
17/10/10 08:26:53 INFO mapreduce.Job:  map 40% reduce 0%
17/10/10 08:26:54 INFO mapreduce.Job:  map 41% reduce 0%
17/10/10 08:26:59 INFO mapreduce.Job:  map 44% reduce 0%
17/10/10 08:27:00 INFO mapreduce.Job:  map 46% reduce 0%
17/10/10 08:27:05 INFO mapreduce.Job:  map 49% reduce 0%
17/10/10 08:27:06 INFO mapreduce.Job:  map 50% reduce 0%
17/10/10 08:27:11 INFO mapreduce.Job:  map 53% reduce 0%
17/10/10 08:27:13 INFO mapreduce.Job:  map 54% reduce 0%
17/10/10 08:27:18 INFO mapreduce.Job:  map 57% reduce 0%
17/10/10 08:27:19 INFO mapreduce.Job:  map 59% reduce 0%
17/10/10 08:27:24 INFO mapreduce.Job:  map 62% reduce 0%
17/10/10 08:27:25 INFO mapreduce.Job:  map 63% reduce 0%
17/10/10 08:27:30 INFO mapreduce.Job:  map 66% reduce 0%
17/10/10 08:27:31 INFO mapreduce.Job:  map 67% reduce 0%
17/10/10 08:27:35 INFO mapreduce.Job:  map 69% reduce 0%
17/10/10 08:27:37 INFO mapreduce.Job:  map 71% reduce 0%
17/10/10 08:27:41 INFO mapreduce.Job:  map 74% reduce 0%
17/10/10 08:27:48 INFO mapreduce.Job:  map 77% reduce 0%
17/10/10 08:27:54 INFO mapreduce.Job:  map 81% reduce 0%
17/10/10 08:28:00 INFO mapreduce.Job:  map 84% reduce 0%
17/10/10 08:28:06 INFO mapreduce.Job:  map 88% reduce 0%
17/10/10 08:28:12 INFO mapreduce.Job:  map 91% reduce 0%
17/10/10 08:28:18 INFO mapreduce.Job:  map 95% reduce 0%
17/10/10 08:28:23 INFO mapreduce.Job:  map 96% reduce 0%
17/10/10 08:28:24 INFO mapreduce.Job:  map 98% reduce 0%
17/10/10 08:28:28 INFO mapreduce.Job:  map 100% reduce 0%
17/10/10 08:28:29 INFO mapreduce.Job: Job job_1507634065337_0001 completed succe                                                                                                                               ssfully
17/10/10 08:28:29 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=500032
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10737418200
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=551387
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=551387
                Total vcore-seconds taken by all map tasks=551387
                Total megabyte-seconds taken by all map tasks=564620288
        Map-Reduce Framework
                Map input records=107374182
                Map output records=107374182
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1424
                CPU time spent (ms)=161010
                Physical memory (bytes) snapshot=904237056
                Virtual memory (bytes) snapshot=6272942080
                Total committed heap usage (bytes)=825753600
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=230593859918397906
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10737418200

real    2m46.037s
user    0m6.343s
sys     0m0.386s


[egruppioni@ip-172-31-26-219 root]$ time hadoop jar /opt/cloudera/parcels/CDH/ja                                                                                                                               rs/hadoop-examples.jar terasort teragen
17/10/10 08:31:02 INFO terasort.TeraSort: starting
java.lang.ArrayIndexOutOfBoundsException: 1
        at org.apache.hadoop.examples.terasort.TeraSort.run(TeraSort.java:284)
        at org.apache.hadoop.util.ToolRunner.run(ToolRunner.java:70)
        at org.apache.hadoop.examples.terasort.TeraSort.main(TeraSort.java:325)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.                                                                                                                               java:57)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAcces                                                                                                                               sorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:606)
        at org.apache.hadoop.util.ProgramDriver$ProgramDescription.invoke(Progra                                                                                                                               mDriver.java:71)
        at org.apache.hadoop.util.ProgramDriver.run(ProgramDriver.java:144)
        at org.apache.hadoop.examples.ExampleDriver.main(ExampleDriver.java:74)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.                                                                                                                               java:57)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAcces                                                                                                                               sorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:606)
        at org.apache.hadoop.util.RunJar.run(RunJar.java:221)
        at org.apache.hadoop.util.RunJar.main(RunJar.java:136)

real    0m1.377s
user    0m2.261s
sys     0m0.230s
You have mail in /var/spool/mail/root
[egruppioni@ip-172-31-26-219 root]$ time hadoop jar /opt/cloudera/parcels/CDH/ja                                                                                                                               rs/hadoop-examples.jar terasort teragen teragen
17/10/10 08:31:14 INFO terasort.TeraSort: starting
17/10/10 08:31:16 INFO input.FileInputFormat: Total input paths to process : 4
Spent 382ms computing base-splits.
Spent 7ms computing TeraScheduler splits.
Computing input splits took 390ms
Sampling 10 splits of 320
Making 8 from 100000 sampled records
Computing parititions took 1010ms
Spent 1402ms computing partitions.
17/10/10 08:31:17 INFO client.RMProxy: Connecting to ResourceManager at ip-172-3                                                                                                                               1-18-42.eu-central-1.compute.internal/172.31.18.42:8032
17/10/10 08:31:18 INFO mapreduce.JobSubmitter: number of splits:320
17/10/10 08:31:18 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_15                                                                                                                               07634065337_0002
17/10/10 08:31:18 INFO impl.YarnClientImpl: Submitted application application_15                                                                                                                               07634065337_0002
17/10/10 08:31:18 INFO mapreduce.Job: The url to track the job: http://ip-172-31                                                                                                                               -18-42.eu-central-1.compute.internal:8088/proxy/application_1507634065337_0002/
17/10/10 08:31:18 INFO mapreduce.Job: Running job: job_1507634065337_0002
17/10/10 08:31:25 INFO mapreduce.Job: Job job_1507634065337_0002 running in uber                                                                                                                                mode : false
17/10/10 08:31:25 INFO mapreduce.Job:  map 0% reduce 0%
17/10/10 08:31:38 INFO mapreduce.Job:  map 2% reduce 0%
17/10/10 08:31:39 INFO mapreduce.Job:  map 3% reduce 0%
17/10/10 08:31:42 INFO mapreduce.Job:  map 4% reduce 0%
17/10/10 08:31:47 INFO mapreduce.Job:  map 5% reduce 0%
17/10/10 08:31:48 INFO mapreduce.Job:  map 6% reduce 0%
17/10/10 08:31:49 INFO mapreduce.Job:  map 7% reduce 0%
17/10/10 08:31:56 INFO mapreduce.Job:  map 8% reduce 0%
17/10/10 08:31:57 INFO mapreduce.Job:  map 9% reduce 0%
17/10/10 08:31:58 INFO mapreduce.Job:  map 10% reduce 0%
17/10/10 08:31:59 INFO mapreduce.Job:  map 11% reduce 0%
17/10/10 08:32:07 INFO mapreduce.Job:  map 12% reduce 0%
17/10/10 08:32:08 INFO mapreduce.Job:  map 13% reduce 0%
17/10/10 08:32:10 INFO mapreduce.Job:  map 15% reduce 0%
17/10/10 08:32:17 INFO mapreduce.Job:  map 16% reduce 0%
17/10/10 08:32:18 INFO mapreduce.Job:  map 17% reduce 0%
17/10/10 08:32:19 INFO mapreduce.Job:  map 18% reduce 0%
17/10/10 08:32:24 INFO mapreduce.Job:  map 19% reduce 0%
17/10/10 08:32:27 INFO mapreduce.Job:  map 20% reduce 0%
17/10/10 08:32:28 INFO mapreduce.Job:  map 21% reduce 0%
17/10/10 08:32:29 INFO mapreduce.Job:  map 22% reduce 0%
17/10/10 08:32:36 INFO mapreduce.Job:  map 23% reduce 0%
17/10/10 08:32:37 INFO mapreduce.Job:  map 24% reduce 0%
17/10/10 08:32:38 INFO mapreduce.Job:  map 25% reduce 0%
17/10/10 08:32:39 INFO mapreduce.Job:  map 26% reduce 0%
17/10/10 08:32:45 INFO mapreduce.Job:  map 27% reduce 0%
17/10/10 08:32:48 INFO mapreduce.Job:  map 28% reduce 0%
17/10/10 08:32:49 INFO mapreduce.Job:  map 29% reduce 0%
17/10/10 08:32:52 INFO mapreduce.Job:  map 30% reduce 0%
17/10/10 08:32:55 INFO mapreduce.Job:  map 31% reduce 0%
17/10/10 08:32:58 INFO mapreduce.Job:  map 32% reduce 0%
17/10/10 08:32:59 INFO mapreduce.Job:  map 33% reduce 0%
17/10/10 08:33:04 INFO mapreduce.Job:  map 34% reduce 0%
17/10/10 08:33:05 INFO mapreduce.Job:  map 35% reduce 0%
17/10/10 08:33:08 INFO mapreduce.Job:  map 36% reduce 0%
17/10/10 08:33:09 INFO mapreduce.Job:  map 37% reduce 0%
17/10/10 08:33:13 INFO mapreduce.Job:  map 38% reduce 0%
17/10/10 08:33:17 INFO mapreduce.Job:  map 39% reduce 0%
17/10/10 08:33:18 INFO mapreduce.Job:  map 40% reduce 0%
17/10/10 08:33:20 INFO mapreduce.Job:  map 41% reduce 0%
17/10/10 08:33:22 INFO mapreduce.Job:  map 42% reduce 0%
17/10/10 08:33:26 INFO mapreduce.Job:  map 43% reduce 0%
17/10/10 08:33:29 INFO mapreduce.Job:  map 44% reduce 0%
17/10/10 08:33:31 INFO mapreduce.Job:  map 45% reduce 0%
17/10/10 08:33:33 INFO mapreduce.Job:  map 46% reduce 0%
17/10/10 08:33:36 INFO mapreduce.Job:  map 47% reduce 0%
17/10/10 08:33:39 INFO mapreduce.Job:  map 48% reduce 0%
17/10/10 08:33:42 INFO mapreduce.Job:  map 49% reduce 0%
17/10/10 08:33:45 INFO mapreduce.Job:  map 50% reduce 0%
17/10/10 08:33:46 INFO mapreduce.Job:  map 51% reduce 0%
17/10/10 08:33:48 INFO mapreduce.Job:  map 52% reduce 0%
17/10/10 08:33:52 INFO mapreduce.Job:  map 53% reduce 0%
17/10/10 08:33:56 INFO mapreduce.Job:  map 54% reduce 0%
17/10/10 08:33:59 INFO mapreduce.Job:  map 55% reduce 0%
17/10/10 08:34:00 INFO mapreduce.Job:  map 56% reduce 0%
17/10/10 08:34:02 INFO mapreduce.Job:  map 57% reduce 0%
17/10/10 08:34:06 INFO mapreduce.Job:  map 58% reduce 0%
17/10/10 08:34:08 INFO mapreduce.Job:  map 59% reduce 0%
17/10/10 08:34:12 INFO mapreduce.Job:  map 60% reduce 0%
17/10/10 08:34:14 INFO mapreduce.Job:  map 61% reduce 0%
17/10/10 08:34:17 INFO mapreduce.Job:  map 62% reduce 0%
17/10/10 08:34:18 INFO mapreduce.Job:  map 63% reduce 0%
17/10/10 08:34:22 INFO mapreduce.Job:  map 64% reduce 0%
17/10/10 08:34:25 INFO mapreduce.Job:  map 65% reduce 0%
17/10/10 08:34:27 INFO mapreduce.Job:  map 66% reduce 0%
17/10/10 08:34:28 INFO mapreduce.Job:  map 67% reduce 0%
17/10/10 08:34:30 INFO mapreduce.Job:  map 68% reduce 0%
17/10/10 08:34:35 INFO mapreduce.Job:  map 69% reduce 0%
17/10/10 08:34:38 INFO mapreduce.Job:  map 70% reduce 0%
17/10/10 08:34:40 INFO mapreduce.Job:  map 71% reduce 0%
17/10/10 08:34:41 INFO mapreduce.Job:  map 72% reduce 0%
17/10/10 08:34:45 INFO mapreduce.Job:  map 73% reduce 0%
17/10/10 08:34:48 INFO mapreduce.Job:  map 74% reduce 0%
17/10/10 08:34:49 INFO mapreduce.Job:  map 75% reduce 0%
17/10/10 08:34:53 INFO mapreduce.Job:  map 76% reduce 0%
17/10/10 08:34:56 INFO mapreduce.Job:  map 77% reduce 0%
17/10/10 08:34:58 INFO mapreduce.Job:  map 78% reduce 0%
17/10/10 08:35:01 INFO mapreduce.Job:  map 79% reduce 0%
17/10/10 08:35:05 INFO mapreduce.Job:  map 80% reduce 0%
17/10/10 08:35:06 INFO mapreduce.Job:  map 81% reduce 0%
17/10/10 08:35:07 INFO mapreduce.Job:  map 82% reduce 0%
17/10/10 08:35:11 INFO mapreduce.Job:  map 83% reduce 0%
17/10/10 08:35:16 INFO mapreduce.Job:  map 84% reduce 0%
17/10/10 08:35:17 INFO mapreduce.Job:  map 85% reduce 0%
17/10/10 08:35:25 INFO mapreduce.Job:  map 85% reduce 3%
17/10/10 08:35:26 INFO mapreduce.Job:  map 85% reduce 8%
17/10/10 08:35:27 INFO mapreduce.Job:  map 86% reduce 11%
17/10/10 08:35:30 INFO mapreduce.Job:  map 87% reduce 13%
17/10/10 08:35:31 INFO mapreduce.Job:  map 87% reduce 14%
17/10/10 08:35:32 INFO mapreduce.Job:  map 87% reduce 16%
17/10/10 08:35:33 INFO mapreduce.Job:  map 87% reduce 22%
17/10/10 08:35:35 INFO mapreduce.Job:  map 88% reduce 22%
17/10/10 08:35:36 INFO mapreduce.Job:  map 88% reduce 23%
17/10/10 08:35:38 INFO mapreduce.Job:  map 88% reduce 24%
17/10/10 08:35:39 INFO mapreduce.Job:  map 88% reduce 26%
17/10/10 08:35:42 INFO mapreduce.Job:  map 89% reduce 26%
17/10/10 08:35:43 INFO mapreduce.Job:  map 90% reduce 26%
17/10/10 08:35:48 INFO mapreduce.Job:  map 91% reduce 26%
17/10/10 08:35:51 INFO mapreduce.Job:  map 92% reduce 26%
17/10/10 08:35:54 INFO mapreduce.Job:  map 93% reduce 27%
17/10/10 08:35:59 INFO mapreduce.Job:  map 94% reduce 27%
17/10/10 08:36:05 INFO mapreduce.Job:  map 95% reduce 27%
17/10/10 08:36:06 INFO mapreduce.Job:  map 96% reduce 28%
17/10/10 08:36:11 INFO mapreduce.Job:  map 97% reduce 28%
17/10/10 08:36:14 INFO mapreduce.Job:  map 98% reduce 28%
17/10/10 08:36:18 INFO mapreduce.Job:  map 99% reduce 28%
17/10/10 08:36:20 INFO mapreduce.Job:  map 99% reduce 29%
17/10/10 08:36:23 INFO mapreduce.Job:  map 100% reduce 29%
17/10/10 08:36:25 INFO mapreduce.Job:  map 100% reduce 30%
17/10/10 08:36:26 INFO mapreduce.Job:  map 100% reduce 33%
17/10/10 08:36:27 INFO mapreduce.Job:  map 100% reduce 40%
17/10/10 08:36:30 INFO mapreduce.Job:  map 100% reduce 45%
17/10/10 08:36:31 INFO mapreduce.Job:  map 100% reduce 48%
17/10/10 08:36:32 INFO mapreduce.Job:  map 100% reduce 55%
17/10/10 08:36:33 INFO mapreduce.Job:  map 100% reduce 63%
17/10/10 08:36:34 INFO mapreduce.Job:  map 100% reduce 67%
17/10/10 08:36:36 INFO mapreduce.Job:  map 100% reduce 68%
17/10/10 08:36:38 INFO mapreduce.Job:  map 100% reduce 72%
17/10/10 08:36:39 INFO mapreduce.Job:  map 100% reduce 76%
17/10/10 08:36:40 INFO mapreduce.Job:  map 100% reduce 77%
17/10/10 08:36:41 INFO mapreduce.Job:  map 100% reduce 78%
17/10/10 08:36:42 INFO mapreduce.Job:  map 100% reduce 80%
17/10/10 08:36:44 INFO mapreduce.Job:  map 100% reduce 82%
17/10/10 08:36:45 INFO mapreduce.Job:  map 100% reduce 87%
17/10/10 08:36:46 INFO mapreduce.Job:  map 100% reduce 91%
17/10/10 08:36:47 INFO mapreduce.Job:  map 100% reduce 92%
17/10/10 08:36:50 INFO mapreduce.Job:  map 100% reduce 94%
17/10/10 08:36:52 INFO mapreduce.Job:  map 100% reduce 95%
17/10/10 08:36:54 INFO mapreduce.Job:  map 100% reduce 96%
17/10/10 08:36:55 INFO mapreduce.Job:  map 100% reduce 97%
17/10/10 08:36:58 INFO mapreduce.Job:  map 100% reduce 98%
17/10/10 08:37:05 INFO mapreduce.Job:  map 100% reduce 100%
17/10/10 08:37:05 INFO mapreduce.Job: Job job_1507634065337_0002 completed succe                                                                                                                               ssfully
17/10/10 08:37:05 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=4805502646
                FILE: Number of bytes written=9544592992
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10737469080
                HDFS: Number of bytes written=10737418200
                HDFS: Number of read operations=984
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=320
                Launched reduce tasks=8
                Data-local map tasks=320
                Total time spent by all maps in occupied slots (ms)=2978389
                Total time spent by all reduces in occupied slots (ms)=734136
                Total time spent by all map tasks (ms)=2978389
                Total time spent by all reduce tasks (ms)=734136
                Total vcore-seconds taken by all map tasks=2978389
                Total vcore-seconds taken by all reduce tasks=734136
                Total megabyte-seconds taken by all map tasks=3049870336
                Total megabyte-seconds taken by all reduce tasks=751755264
        Map-Reduce Framework
                Map input records=107374182
                Map output records=107374182
                Map output bytes=10952166564
                Map output materialized bytes=4697595376
                Input split bytes=50880
                Combine input records=0
                Combine output records=0
                Reduce input groups=107374182
                Reduce shuffle bytes=4697595376
                Reduce input records=107374182
                Reduce output records=107374182
                Spilled Records=214748364
                Shuffled Maps =2560
                Failed Shuffles=0
                Merged Map outputs=2560
                GC time elapsed (ms)=42039
                CPU time spent (ms)=1597630
                Physical memory (bytes) snapshot=164152848384
                Virtual memory (bytes) snapshot=513420095488
                Total committed heap usage (bytes)=186527514624
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10737418200
        File Output Format Counters
                Bytes Written=10737418200
17/10/10 08:37:05 INFO terasort.TeraSort: done

real    5m51.274s
user    0m10.211s
sys     0m0.542s

[root@ip-172-31-26-219 ~]# sudo -u hdfs hdfs dfs -ls /user
Found 5 items
drwxr-xr-x   - egruppioni supergroup          0 2017-10-10 08:25 /user/egruppion                                                                                                                               i
drwxrwxrwx   - mapred     hadoop              0 2017-10-10 07:14 /user/history
drwxrwxr-t   - hive       hive                0 2017-10-10 07:15 /user/hive
drwxrwxr-x   - hue        hue                 0 2017-10-10 07:15 /user/hue
drwxrwxr-x   - oozie      oozie               0 2017-10-10 07:15 /user/oozie

[root@ip-172-31-26-219 ~]# sudo -u hdfs hdfs dfs -ls /user/egruppioni
Found 2 items
drwx------   - egruppioni supergroup          0 2017-10-10 08:37 /user/egruppion                                                                                                                               i/.staging
drwxr-xr-x   - egruppioni supergroup          0 2017-10-10 08:37 /user/egruppion                                                                                                                               i/teragen
                                                                                                                            i/teragen/part-r-00007
[root@ip-172-31-26-219 ~]# sudo -u hdfs hdfs dfs -ls /user/egruppioni/teragen
Found 14 items
-rw-r--r--   1 egruppioni supergroup          0 2017-10-10 08:37 /user/egruppioni/teragen/_SUCCESS
-rw-r--r--  10 egruppioni supergroup         77 2017-10-10 08:31 /user/egruppioni/teragen/_partition.lst
-rw-r--r--   3 egruppioni supergroup 2684354600 2017-10-10 08:28 /user/egruppioni/teragen/part-m-00000
-rw-r--r--   3 egruppioni supergroup 2684354500 2017-10-10 08:28 /user/egruppioni/teragen/part-m-00001
-rw-r--r--   3 egruppioni supergroup 2684354600 2017-10-10 08:28 /user/egruppioni/teragen/part-m-00002
-rw-r--r--   3 egruppioni supergroup 2684354500 2017-10-10 08:27 /user/egruppioni/teragen/part-m-00003
-rw-r--r--   1 egruppioni supergroup 1341324400 2017-10-10 08:36 /user/egruppioni/teragen/part-r-00000
-rw-r--r--   1 egruppioni supergroup 1321377000 2017-10-10 08:36 /user/egruppioni/teragen/part-r-00001
-rw-r--r--   1 egruppioni supergroup 1344586900 2017-10-10 08:36 /user/egruppioni/teragen/part-r-00002
-rw-r--r--   1 egruppioni supergroup 1351892700 2017-10-10 08:36 /user/egruppioni/teragen/part-r-00003
-rw-r--r--   1 egruppioni supergroup 1349175000 2017-10-10 08:36 /user/egruppioni/teragen/part-r-00004
-rw-r--r--   1 egruppioni supergroup 1362008100 2017-10-10 08:36 /user/egruppioni/teragen/part-r-00005
-rw-r--r--   1 egruppioni supergroup 1323208300 2017-10-10 08:36 /user/egruppioni/teragen/part-r-00006
-rw-r--r--   1 egruppioni supergroup 1343845800 2017-10-10 08:37 /user/egruppioni/teragen/part-r-00007
```