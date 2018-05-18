time hadoop jar  /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen \
-Dmapred.map.tasks=1 \
-Ddfs.block.size=67108864 \
-Dmapreduce.map.memory.mb=1000 \
5000000000 \
/user/groot/tgen