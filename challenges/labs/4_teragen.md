*Script Teragen
			[cate@mycloudera1 ~]$ hadoop jar  /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen 65536000 cate/tgen640
			17/05/05 04:40:08 INFO client.RMProxy: Connecting to ResourceManager at mycloudera1.jimmy/10.146.0.6:8032
			17/05/05 04:40:08 INFO terasort.TeraGen: Generating 65536000 using 2
			17/05/05 04:40:09 INFO mapreduce.JobSubmitter: number of splits:2
			17/05/05 04:40:10 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493957167216_0001
			17/05/05 04:40:10 INFO impl.YarnClientImpl: Submitted application application_1493957167216_0001
			17/05/05 04:40:10 INFO mapreduce.Job: The url to track the job: http://mycloudera1.jimmy:8088/proxy/application_1493957167216_0001/
			17/05/05 04:40:10 INFO mapreduce.Job: Running job: job_1493957167216_0001
			17/05/05 04:40:19 INFO mapreduce.Job: Job job_1493957167216_0001 running in uber mode : false
			17/05/05 04:40:19 INFO mapreduce.Job:  map 0% reduce 0%
			17/05/05 04:40:38 INFO mapreduce.Job:  map 20% reduce 0%
			17/05/05 04:40:44 INFO mapreduce.Job:  map 34% reduce 0%
			17/05/05 04:40:50 INFO mapreduce.Job:  map 48% reduce 0%
			17/05/05 04:40:56 INFO mapreduce.Job:  map 63% reduce 0%
			17/05/05 04:41:02 INFO mapreduce.Job:  map 76% reduce 0%
			17/05/05 04:41:07 INFO mapreduce.Job:  map 82% reduce 0%
			17/05/05 04:41:08 INFO mapreduce.Job:  map 87% reduce 0%
			17/05/05 04:41:13 INFO mapreduce.Job:  map 97% reduce 0%
			17/05/05 04:41:15 INFO mapreduce.Job:  map 98% reduce 0%
			17/05/05 04:41:16 INFO mapreduce.Job:  map 100% reduce 0%
			17/05/05 04:41:16 INFO mapreduce.Job: Job job_1493957167216_0001 completed successfully
			17/05/05 04:41:17 INFO mapreduce.Job: Counters: 31
					File System Counters
							FILE: Number of bytes read=0
							FILE: Number of bytes written=248972
							FILE: Number of read operations=0
							FILE: Number of large read operations=0
							FILE: Number of write operations=0
							HDFS: Number of bytes read=170
							HDFS: Number of bytes written=6553600000
							HDFS: Number of read operations=8
							HDFS: Number of large read operations=0
							HDFS: Number of write operations=4
					Job Counters
							Launched map tasks=2
							Other local map tasks=2
							Total time spent by all maps in occupied slots (ms)=108145
							Total time spent by all reduces in occupied slots (ms)=0
							Total time spent by all map tasks (ms)=108145
							Total vcore-seconds taken by all map tasks=108145
							Total megabyte-seconds taken by all map tasks=110740480
					Map-Reduce Framework
							Map input records=65536000
							Map output records=65536000
							Input split bytes=170
							Spilled Records=0
							Failed Shuffles=0
							Merged Map outputs=0
							GC time elapsed (ms)=874
							CPU time spent (ms)=99910
							Physical memory (bytes) snapshot=420065280
							Virtual memory (bytes) snapshot=3133198336
							Total committed heap usage (bytes)=376438784
					org.apache.hadoop.examples.terasort.TeraGen$Counters
							CHECKSUM=140750829423462787
					File Input Format Counters
							Bytes Read=0
					File Output Format Counters
							Bytes Written=6553600000
			[cate@mycloudera1 ~]$


*List result teragen			
[cate@mycloudera1 ~]$ hdfs dfs -ls /user/cate/
Found 2 items
drwx------   - cate supergroup          0 2017-05-05 04:41 /user/cate/.staging
drwxr-xr-x   - cate supergroup          0 2017-05-05 04:40 /user/cate/cate
[cate@mycloudera1 ~]$
