```
command to generate input file for teragen
time hadoop jar hadoop-examples.jar teragen -D dfs.blocksize.size=33554432 107374182 /user/heatonjmark/heatonjmark1
*****************************************************************************
Time for data generation
real    2m44.873s
user    0m6.036s
sys     0m0.254s
Time for Teragen
*****************************************************************************
Command for terasort
time hadoop jar hadoop-examples.jar terasort  /user/heatonjmark/heatonjmark1 /user/heatonjmark/heatonjmark-sorted
****************************************************************************
Time for sort without cache pool
real    3m2.860s
user    0m8.705s
sys     0m0.348s
****************************************************************************
time hadoop jar hadoop-examples.jar terasort  /user/heatonjmark/heatonjmark1 /user/heatonjmark/heatonjmark-sorted
******************************************************************************
commands to turn on cachePool
hdfs cacheadmin  -addPool swimming
hdfs cacheadmin -addDirective -path /user/heatonjmark/heatonjmark1 -pool swimming
*****************************************************************************
command for terasort
time hadoop jar hadoop-examples.jar terasort  /user/heatonjmark/heatonjmark1 /user/heatonjmark/heatonjmark-sorted1
*****************************************************************************
command for terasort
time hadoop jar hadoop-examples.jar terasort  /user/heatonjmark/heatonjmark1 /user/heatonjmark/heatonjmark-sorted1
******************************************************************************
Time for terasort with cachePool
real    2m56.551s
user    0m8.452s
sys     0m0.364s
```
