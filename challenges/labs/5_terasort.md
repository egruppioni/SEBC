```   
[root@ip-172-31-8-36 ~]# kinit jimenez
Password for jimenez@EGRUPPIONI.TX:
[root@ip-172-31-8-36 ~]# time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar terasort tgen tsort
17/10/13 04:46:07 INFO terasort.TeraSort: starting
17/10/13 04:46:08 INFO hdfs.DFSClient: Created token for jimenez: HDFS_DELEGATION_TOKEN owner=jimenez@EGRUPPIONI.TX, renewer=yarn, realUser=, issueDate=1507884368710, maxDate=1508489168710, sequenceNumber=2, masterKeyId=2 on 172.31.15.151:8020
17/10/13 04:46:08 INFO security.TokenCache: Got dt for hdfs://ip-172-31-15-151.eu-central-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.15.151:8020, Ident: (token for jimenez: HDFS_DELEGATION_TOKEN owner=jimenez@EGRUPPIONI.TX, renewer=yarn, realUser=, issueDate=1507884368710, maxDate=1508489168710, sequenceNumber=2, masterKeyId=2)
17/10/13 04:46:08 INFO input.FileInputFormat: Total input paths to process : 8
Spent 344ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 349ms
Sampling 10 splits of 104
Making 8 from 100000 sampled records
Computing parititions took 747ms
Spent 1098ms computing partitions.
17/10/13 04:46:09 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-15-151.eu-central-1.compute.internal/172.31.15.151:8032
17/10/13 04:46:10 INFO mapreduce.JobSubmitter: number of splits:104
17/10/13 04:46:10 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507884177958_0001
17/10/13 04:46:10 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.15.151:8020, Ident: (token for jimenez: HDFS_DELEGATION_TOKEN owner=jimenez@EGRUPPIONI.TX, renewer=yarn, realUser=, issueDate=1507884368710, maxDate=1508489168710, sequenceNumber=2, masterKeyId=2)
17/10/13 04:46:11 INFO impl.YarnClientImpl: Submitted application application_1507884177958_0001
17/10/13 04:46:11 INFO mapreduce.Job: The url to track the job: http://ip-172-31-15-151.eu-central-1.compute.internal:8088/proxy/application_1507884177958_0001/
17/10/13 04:46:11 INFO mapreduce.Job: Running job: job_1507884177958_0001
17/10/13 04:46:21 INFO mapreduce.Job: Job job_1507884177958_0001 running in uber mode : false
17/10/13 04:46:21 INFO mapreduce.Job:  map 0% reduce 0%
17/10/13 04:46:29 INFO mapreduce.Job:  map 1% reduce 0%
17/10/13 04:46:35 INFO mapreduce.Job:  map 3% reduce 0%
17/10/13 04:46:36 INFO mapreduce.Job:  map 4% reduce 0%
17/10/13 04:46:39 INFO mapreduce.Job:  map 6% reduce 0%
17/10/13 04:46:40 INFO mapreduce.Job:  map 10% reduce 0%
17/10/13 04:46:43 INFO mapreduce.Job:  map 12% reduce 0%
17/10/13 04:46:44 INFO mapreduce.Job:  map 13% reduce 0%
17/10/13 04:46:50 INFO mapreduce.Job:  map 14% reduce 0%
17/10/13 04:46:51 INFO mapreduce.Job:  map 17% reduce 0%
17/10/13 04:46:52 INFO mapreduce.Job:  map 18% reduce 0%
17/10/13 04:46:53 INFO mapreduce.Job:  map 21% reduce 0%
17/10/13 04:46:58 INFO mapreduce.Job:  map 22% reduce 0%
17/10/13 04:47:01 INFO mapreduce.Job:  map 23% reduce 0%
17/10/13 04:47:02 INFO mapreduce.Job:  map 25% reduce 0%
17/10/13 04:47:03 INFO mapreduce.Job:  map 26% reduce 0%
17/10/13 04:47:04 INFO mapreduce.Job:  map 27% reduce 0%
17/10/13 04:47:05 INFO mapreduce.Job:  map 31% reduce 0%
17/10/13 04:47:11 INFO mapreduce.Job:  map 32% reduce 0%
17/10/13 04:47:12 INFO mapreduce.Job:  map 34% reduce 0%
17/10/13 04:47:14 INFO mapreduce.Job:  map 35% reduce 0%
17/10/13 04:47:15 INFO mapreduce.Job:  map 36% reduce 0%
17/10/13 04:47:16 INFO mapreduce.Job:  map 38% reduce 0%
17/10/13 04:47:17 INFO mapreduce.Job:  map 39% reduce 0%
17/10/13 04:47:19 INFO mapreduce.Job:  map 40% reduce 0%
17/10/13 04:47:20 INFO mapreduce.Job:  map 42% reduce 0%
17/10/13 04:47:25 INFO mapreduce.Job:  map 43% reduce 0%
17/10/13 04:47:26 INFO mapreduce.Job:  map 46% reduce 0%
17/10/13 04:47:27 INFO mapreduce.Job:  map 48% reduce 0%
17/10/13 04:47:28 INFO mapreduce.Job:  map 49% reduce 0%
17/10/13 04:47:29 INFO mapreduce.Job:  map 51% reduce 0%
17/10/13 04:47:33 INFO mapreduce.Job:  map 52% reduce 0%
17/10/13 04:47:36 INFO mapreduce.Job:  map 53% reduce 0%
17/10/13 04:47:37 INFO mapreduce.Job:  map 55% reduce 0%
17/10/13 04:47:38 INFO mapreduce.Job:  map 59% reduce 0%
17/10/13 04:47:39 INFO mapreduce.Job:  map 60% reduce 0%
17/10/13 04:47:40 INFO mapreduce.Job:  map 61% reduce 0%
17/10/13 04:47:47 INFO mapreduce.Job:  map 64% reduce 0%
17/10/13 04:47:48 INFO mapreduce.Job:  map 65% reduce 0%
17/10/13 04:47:49 INFO mapreduce.Job:  map 67% reduce 0%
17/10/13 04:47:50 INFO mapreduce.Job:  map 68% reduce 0%
17/10/13 04:47:51 INFO mapreduce.Job:  map 69% reduce 0%
17/10/13 04:47:53 INFO mapreduce.Job:  map 70% reduce 0%
17/10/13 04:47:56 INFO mapreduce.Job:  map 72% reduce 0%
17/10/13 04:47:57 INFO mapreduce.Job:  map 73% reduce 0%
17/10/13 04:47:59 INFO mapreduce.Job:  map 74% reduce 0%
17/10/13 04:48:00 INFO mapreduce.Job:  map 75% reduce 0%
17/10/13 04:48:01 INFO mapreduce.Job:  map 78% reduce 0%
17/10/13 04:48:02 INFO mapreduce.Job:  map 79% reduce 0%
17/10/13 04:48:05 INFO mapreduce.Job:  map 81% reduce 0%
17/10/13 04:48:07 INFO mapreduce.Job:  map 83% reduce 0%
17/10/13 04:48:10 INFO mapreduce.Job:  map 84% reduce 0%
17/10/13 04:48:11 INFO mapreduce.Job:  map 85% reduce 0%
17/10/13 04:48:12 INFO mapreduce.Job:  map 87% reduce 0%
17/10/13 04:48:13 INFO mapreduce.Job:  map 88% reduce 0%
17/10/13 04:48:14 INFO mapreduce.Job:  map 89% reduce 0%
17/10/13 04:48:15 INFO mapreduce.Job:  map 90% reduce 0%
17/10/13 04:48:17 INFO mapreduce.Job:  map 91% reduce 0%
17/10/13 04:48:19 INFO mapreduce.Job:  map 92% reduce 0%
17/10/13 04:48:22 INFO mapreduce.Job:  map 94% reduce 0%
17/10/13 04:48:23 INFO mapreduce.Job:  map 94% reduce 2%
17/10/13 04:48:24 INFO mapreduce.Job:  map 94% reduce 5%
17/10/13 04:48:25 INFO mapreduce.Job:  map 94% reduce 11%
17/10/13 04:48:26 INFO mapreduce.Job:  map 94% reduce 15%
17/10/13 04:48:27 INFO mapreduce.Job:  map 96% reduce 17%
17/10/13 04:48:28 INFO mapreduce.Job:  map 97% reduce 18%
17/10/13 04:48:29 INFO mapreduce.Job:  map 98% reduce 20%
17/10/13 04:48:32 INFO mapreduce.Job:  map 100% reduce 20%
17/10/13 04:48:33 INFO mapreduce.Job:  map 100% reduce 21%
17/10/13 04:48:34 INFO mapreduce.Job:  map 100% reduce 28%
17/10/13 04:48:35 INFO mapreduce.Job:  map 100% reduce 37%
17/10/13 04:48:37 INFO mapreduce.Job:  map 100% reduce 42%
17/10/13 04:48:38 INFO mapreduce.Job:  map 100% reduce 43%
17/10/13 04:48:39 INFO mapreduce.Job:  map 100% reduce 46%
17/10/13 04:48:40 INFO mapreduce.Job:  map 100% reduce 52%
17/10/13 04:48:41 INFO mapreduce.Job:  map 100% reduce 54%
17/10/13 04:48:42 INFO mapreduce.Job:  map 100% reduce 60%
17/10/13 04:48:43 INFO mapreduce.Job:  map 100% reduce 64%
17/10/13 04:48:44 INFO mapreduce.Job:  map 100% reduce 66%
17/10/13 04:48:45 INFO mapreduce.Job:  map 100% reduce 70%
17/10/13 04:48:46 INFO mapreduce.Job:  map 100% reduce 76%
17/10/13 04:48:47 INFO mapreduce.Job:  map 100% reduce 78%
17/10/13 04:48:48 INFO mapreduce.Job:  map 100% reduce 85%
17/10/13 04:48:49 INFO mapreduce.Job:  map 100% reduce 86%
17/10/13 04:48:50 INFO mapreduce.Job:  map 100% reduce 88%
17/10/13 04:48:51 INFO mapreduce.Job:  map 100% reduce 89%
17/10/13 04:48:52 INFO mapreduce.Job:  map 100% reduce 90%
17/10/13 04:48:53 INFO mapreduce.Job:  map 100% reduce 94%
17/10/13 04:48:54 INFO mapreduce.Job:  map 100% reduce 95%
17/10/13 04:48:56 INFO mapreduce.Job:  map 100% reduce 97%
17/10/13 04:48:57 INFO mapreduce.Job:  map 100% reduce 98%
17/10/13 04:49:00 INFO mapreduce.Job:  map 100% reduce 99%
17/10/13 04:49:02 INFO mapreduce.Job:  map 100% reduce 100%
17/10/13 04:49:03 INFO mapreduce.Job: Job job_1507884177958_0001 completed successfully
17/10/13 04:49:03 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2933073204
                FILE: Number of bytes written=5820264980
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553616016
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=336
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=104
                Launched reduce tasks=8
                Data-local map tasks=104
                Total time spent by all maps in occupied slots (ms)=942157
                Total time spent by all reduces in occupied slots (ms)=268331
                Total time spent by all map tasks (ms)=942157
                Total time spent by all reduce tasks (ms)=268331
                Total vcore-seconds taken by all map tasks=942157
                Total vcore-seconds taken by all reduce tasks=268331
                Total megabyte-seconds taken by all map tasks=964768768
                Total megabyte-seconds taken by all reduce tasks=274770944
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2873221966
                Input split bytes=16016
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2873221966
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =832
                Failed Shuffles=0
                Merged Map outputs=832
                GC time elapsed (ms)=17148
                CPU time spent (ms)=729460
                Physical memory (bytes) snapshot=58698395648
                Virtual memory (bytes) snapshot=176186298368
                Total committed heap usage (bytes)=65806008320
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=6553600000
        File Output Format Counters
                Bytes Written=6553600000
17/10/13 04:49:03 INFO terasort.TeraSort: done

real    2m57.898s
user    0m8.186s
sys     0m0.372s
[root@ip-172-31-8-36 ~]#

```   