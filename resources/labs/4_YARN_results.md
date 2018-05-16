# Fastest
```
[centos@ip-172-31-10-250 ~]$ time ./sample.sh
Testing loop started on Wed May 16 20:13:56 UTC 2018
mappers=8
reducers=1
container mem=1048
MAP_MB=838
RED_MB=838
Running 'teragen'

real    0m54.725s
user    0m7.486s
sys     0m0.596s
Running 'terasort'

real    0m2.650s
user    0m4.499s
sys     0m0.430s
Deleted /tg-10GB-8-1-1048
rm: `/ts-10GB-8-1-1048': No such file or directory

real    1m2.643s
user    0m21.193s
sys     0m1.828s
```

# Slowest

```
[centos@ip-172-31-10-250 ~]$ time ./sample.sh
Testing loop started on Wed May 16 20:11:48 UTC 2018
mappers=8
reducers=8
container mem=3048
MAP_MB=2438
RED_MB=2438
Running 'teragen'

real    1m10.404s
user    0m7.696s
sys     0m0.583s
Running 'terasort'

real    0m2.669s
user    0m4.539s
sys     0m0.438s
Deleted /tg-10GB-8-8-3048
rm: `/ts-10GB-8-8-3048': No such file or directory

real    1m18.338s
user    0m21.332s
sys     0m1.877s
```