 1 vm.swappiness
 -----------
 
 `
[root@ip-172-31-24-105 ~]# cat /proc/sys/vm/swappiness
60
[root@ip-172-31-24-105 ~]# sysctl vm.swappiness=1
vm.swappiness = 1
[root@ip-172-31-24-105 ~]# cat /proc/sys/vm/swappiness
1
 `
 
  2 volume mount attributes
 -----------
 
  ```
  [root@ip-172-31-24-105 ~]# cat /etc/fstab

#
# /etc/fstab
# Created by anaconda on Tue Jul 14 09:33:08 2015
#
# Accessible filesystems, by reference, are maintained under '/dev/disk'
# See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info
#
UUID=0e6b1614-7bbe-4d6e-bc78-a5556a123ba8 /                       ext4    defaults        1 1
tmpfs                   /dev/shm                tmpfs   defaults        0 0
devpts                  /dev/pts                devpts  gid=5,mode=620  0 0
sysfs                   /sys                    sysfs   defaults        0 0
proc                    /proc                   proc    defaults        0 0
  ```
  
   3 reserve space
 -----------
 
 `
 [root@ip-172-31-24-105 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       30G  1.7G   27G   6% /
tmpfs           7.3G     0  7.3G   0% /dev/shm
 `
 
    4 disable transparent_hugepage
 -----------
  `
[root@ip-172-31-24-105 ~]# echo never > /sys/kernel/mm/transparent_hugepage/defrag
[root@ip-172-31-24-105 ~]# echo never > /sys/kernel/mm/transparent_hugepage/enabled
`

5 List your network interface configuration
 -----------
  ```
  [root@ip-172-31-24-105 ~]# ifconfig
eth0      Link encap:Ethernet  HWaddr 06:60:44:4B:30:9E
          inet addr:172.31.24.105  Bcast:172.31.31.255  Mask:255.255.240.0
          inet6 addr: fe80::460:44ff:fe4b:309e/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:457 errors:0 dropped:0 overruns:0 frame:0
          TX packets:473 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:41875 (40.8 KiB)  TX bytes:50247 (49.0 KiB)
          Interrupt:145

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

```

6 Show that forward and reverse host lookups are correctly resolved
 -----------
 ```
 [root@ip-172-31-24-105 ~]# nslookup ip-172-31-24-105
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ip-172-31-24-105.eu-central-1.compute.internal
Address: 172.31.24.105

[root@ip-172-31-24-105 ~]# nslookup 172.31.24.105
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
105.24.31.172.in-addr.arpa      name = ip-172-31-24-105.eu-central-1.compute.internal.

Authoritative answers can be found from:
```

6b Show the nscd service is running
 -----------
 `
[root@ip-172-31-24-105 ~]# service nscd start
Starting nscd:                                             [  OK  ]
[root@ip-172-31-24-105 ~]# service nscd status
nscd (pid 24122) is running...
`

7 Show the ntpd service is running
 -----------
  `
[root@ip-172-31-24-105 ~]# service ntpd start
Starting ntpd:                                             [  OK  ]
[root@ip-172-31-24-105 ~]# service ntpd status
ntpd (pid  24174) is running...
 `
