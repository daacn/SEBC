# TeraGen
> time hadoop jar hadoop-examples.jar teragen -D mapred.map.tasks=4 -D dfs.block.size=33554432  100000000 /user/daniel/teragen  

Result of time:
> real    2m42.082s  
> user    0m6.270s  
> sys     0m0.404s  
  
# TeraSort
> time hadoop jar hadoop-examples.jar terasort /user/daniel/teragen /user/daniel/terasort_res  
  
Result of time:  
> real    6m2.784s  
> user    0m9.993s  
> sys     0m0.364s  
