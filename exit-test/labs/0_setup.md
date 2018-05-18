# Cloud provider: AWS


# Servers 

ip-172-31-2-224.us-west-2.compute.internal
[root@ip-172-31-2-224 centos]# uptime
 03:32:49 up 18 min,  1 user,  load average: 0.00, 0.01, 0.02

ip-172-31-14-245.us-west-2.compute.internal
[root@ip-172-31-14-245 centos]# uptime
 03:33:18 up 8 min,  1 user,  load average: 0.00, 0.01, 0.01

ip-172-31-15-59.us-west-2.compute.internal
[root@ip-172-31-15-59 centos]# uptime
 03:33:35 up 9 min,  1 user,  load average: 0.00, 0.01, 0.02

ip-172-31-5-78.us-west-2.compute.internal
[root@ip-172-31-5-78 centos]# uptime
 03:33:47 up 9 min,  1 user,  load average: 0.00, 0.01, 0.01

ip-172-31-0-110.us-west-2.compute.internal
[root@ip-172-31-0-110 centos]# uptime
 03:34:01 up 9 min,  1 user,  load average: 0.00, 0.03, 0.03

 # LINUX RELEASE, FILE CAPACITY, REPOLIST
 ```
 [root@ip-172-31-2-224 centos]# cat /etc/centos-release
CentOS Linux release 7.5.1804 (Core)
[root@ip-172-31-2-224 centos]# lsblk
NAME    MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  50G  0 disk
└─xvda1 202:1    0  50G  0 part /
[root@ip-172-31-2-224 centos]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirrors.sonic.net
 * extras: centos.s.uw.edu
 * updates: repo1.sea.innoscale.net
repo id                             repo name                             status
base/7/x86_64                       CentOS-7 - Base                       9,911
extras/7/x86_64                     CentOS-7 - Extras                       258
updates/7/x86_64                    CentOS-7 - Updates                      151
repolist: 10,320
[root@ip-172-31-2-224 centos]#
```

# USERS AND GROUPS
```
[root@ip-172-31-2-224 centos]# cat /etc/passwd | grep 'thanos\|hulk\|groot'
thanos:x:2500:2500::/home/thanos:/bin/bash
hulk:x:2600:2600::/home/hulk:/bin/bash
groot:x:2700:2700::/home/groot:/bin/bash
[root@ip-172-31-2-224 centos]# cat /etc/group | grep 'blackorder\|avengers'
blackorder:x:2701:thanos
avengers:x:2702:hulk,groot
```