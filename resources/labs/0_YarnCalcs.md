```

I set the following values in file YarnCalc.xls

Worker vcores	20
Worker spindles	12
Worker RAM	128
Workload factor	1
Worker nodes	10

Next I modified OS memory formula to obtain about 8GB Ram as in yarn-tuning-guide.xlsx.

I also modified OS Vcores from 2 to 1.

I left NodeManage, DataNode, CM Agent with the predefined values.


When I change the workload factor I can see different "-D mapreduce.job.maps mapreduce.job.reduces" values as jobs that the cluster can start per nodes as mappers and reducers.

```