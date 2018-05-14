# Vm swappiness
```
[root@ip-172-31-10-250 centos]# sysctl vm.swappiness=1
vm.swappiness = 1
[root@ip-172-31-10-250 centos]# cat /proc/sys/vm/swappiness
1
[root@ip-172-31-10-250 centos]# cat /etc/sysctl.conf
# sysctl settings are defined through files in
# /usr/lib/sysctl.d/, /run/sysctl.d/, and /etc/sysctl.d/.
#
# Vendors settings live in /usr/lib/sysctl.d/.
# To override a whole file, create a new file with the same in
# /etc/sysctl.d/ and put new settings there. To override
# only specific settings, add a file with a lexically later
# name in /etc/sysctl.d/ and put new settings there.
#
# For more information, see sysctl.conf(5) and sysctl.d(5).
vm.swappiness = 1
```

# Mount Attributes
```
[root@ip-172-31-10-250 centos]# lsblk
NAME    MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  30G  0 disk
└─xvda1 202:1    0  30G  0 part /
[root@ip-172-31-10-250 centos]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       30G  845M   30G   3% /
devtmpfs        7.8G     0  7.8G   0% /dev
tmpfs           7.8G     0  7.8G   0% /dev/shm
tmpfs           7.8G   17M  7.8G   1% /run
tmpfs           7.8G     0  7.8G   0% /sys/fs/cgroup
tmpfs           1.6G     0  1.6G   0% /run/user/0
tmpfs           1.6G     0  1.6G   0% /run/user/1000
```

# Volume Type
```
[root@ip-172-31-10-250 centos]# file -sL /dev/xvda1
/dev/xvda1: SGI XFS filesystem data (blksz 4096, inosz 512, v2 dirs)
```

# Disable Transparent Hugepage Support
```
[centos@ip-172-31-10-250 ~]$ cat /sys/kernel/mm/transparent_hugepage/enabled
always madvise [never]
```

# Network Interface Configuration
```
[root@ip-172-31-10-250 usr]# ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN qlen 1
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: ens3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 9001 qdisc mq state UP qlen 1000
    link/ether 0a:ff:5c:aa:4f:60 brd ff:ff:ff:ff:ff:ff
    inet 172.31.10.250/20 brd 172.31.15.255 scope global dynamic ens3
       valid_lft 2680sec preferred_lft 2680sec
    inet6 fe80::8ff:5cff:feaa:4f60/64 scope link
       valid_lft forever preferred_lft forever
[root@ip-172-31-10-250 usr]# cat /etc/sysconfig/network-scripts/ifcfg-ens3
# Created by cloud-init on instance boot automatically, do not edit.
#
BOOTPROTO=dhcp
DEVICE=ens3
HWADDR=0a:ff:5c:aa:4f:60
ONBOOT=yes
TYPE=Ethernet
USERCTL=no
[root@ip-172-31-10-250 usr]#
```

# nslookup
```
[root@ip-172-31-10-250 ~]# nslookup ip-172-31-10-60
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ip-172-31-10-60.us-west-2.compute.internal
Address: 172.31.10.60

[root@ip-172-31-10-250 ~]# nslookup 172.31.10.60
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
60.10.31.172.in-addr.arpa       name = ip-172-31-10-60.us-west-2.compute.internal.

Authoritative answers can be found from:

[root@ip-172-31-10-250 ~]# nslookup ip-172-31-10-60.us-west-2.compute.internal
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ip-172-31-10-60.us-west-2.compute.internal
Address: 172.31.10.60
```

# nscd