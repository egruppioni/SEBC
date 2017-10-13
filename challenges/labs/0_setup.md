```

AWS EC2

challenge_1;		ec2-52-28-198-110.eu-central-1.compute.amazonaws.com;	52.28.198.110;		ip-172-31-4-206.eu-central-1.compute.internal;	172.31.4.206
challenge_2;		ec2-35-157-100-12.eu-central-1.compute.amazonaws.com;	35.157.100.12;		ip-172-31-15-151.eu-central-1.compute.internal;	172.31.15.151
challenge_3;		ec2-18-194-153-49.eu-central-1.compute.amazonaws.com;	18.194.153.49;		ip-172-31-2-253.eu-central-1.compute.internal;172.31.2.253
challenge_4;		ec2-18-194-133-76.eu-central-1.compute.amazonaws.com;	18.194.133.76;		ip-172-31-8-36.eu-central-1.compute.internal;172.31.8.36
challenge_5;		ec2-18-194-77-18.eu-central-1.compute.amazonaws.com;	18.194.77.18;		ip-172-31-6-246.eu-central-1.compute.internal;172.31.6.246


Red Hat Enterprise Linux (RHEL) 6 (HVM) -RHEL-6.7_HVM-20160219-x86_64-1-Hourly2-GP2 (ami-cd362ca1)
Red Hat Enterprise Linux Server release 6.7 (Santiago)

[root@ip-172-31-4-206 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       30G  2.0G   26G   7% /
tmpfs           7.3G     0  7.3G   0% /dev/shm


[root@ip-172-31-4-206 ~]# yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, security
repo id                                                                               repo name                                                                                                          status
rhui-REGION-client-config-server-6                                                    Red Hat Update Infrastructure 2.0 Client Configuration Server 6                                                         5
rhui-REGION-rhel-server-releases                                                      Red Hat Enterprise Linux Server 6 (RPMs)                                                                           19,784
rhui-REGION-rhel-server-rh-common                                                     Red Hat Enterprise Linux Server 6 RH Common (RPMs)                                                                    129
repolist: 19,918


[root@ip-172-31-4-206 ~]# cat /etc/passwd |grep jimenez
jimenez:x:2800:2800::/home/jimenez:/bin/bash
[root@ip-172-31-4-206 ~]# cat /etc/passwd |grep beltran
beltran:x:2900:2900::/home/beltran:/bin/bash
[root@ip-172-31-4-206 ~]#

[root@ip-172-31-4-206 ~]# cat /etc/group |grep astros
astros:x:2901:beltran
[root@ip-172-31-4-206 ~]# cat /etc/group |grep rangers
rangers:x:2902:jimenez

```