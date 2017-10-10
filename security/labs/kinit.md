[root@ip-172-31-26-219 ~]# kinit egruppioni
kinit: Client not found in Kerberos database while getting initial credentials
[root@ip-172-31-26-219 ~]# kinit egruppioni
Password for egruppioni@EGRUPPIONI.HQ:
[root@ip-172-31-26-219 ~]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: egruppioni@EGRUPPIONI.HQ

Valid starting     Expires            Service principal
10/10/17 12:12:10  10/11/17 12:12:10  krbtgt/EGRUPPIONI.HQ@EGRUPPIONI.HQ
        renew until 10/17/17 12:12:10
[root@ip-172-31-26-219 ~]#
