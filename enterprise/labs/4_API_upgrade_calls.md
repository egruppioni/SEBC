```

Report latest API version

curl -u egruppioni:cloudera 'http://172.31.24.105:7180/api/version' 


[root@ip-172-31-24-105 yum.repos.d]# curl -u egruppioni:cloudera 'http://172.31.24.105:7180/api/version'
v17

Report the CM version

curl -u egruppioni:cloudera 'http://172.31.24.105:7180/api/v17/cm/version'


[root@ip-172-31-24-105 yum.repos.d]# curl -u egruppioni:cloudera 'http://172.31.24.105:7180/api/v17/cm/version'
{
  "version" : "5.12.1",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170818-0807",
  "gitHash" : "9bdee611802535491d400e03c98ef694a2c77d0a",
  "snapshot" : false
}[root@ip-172-31-24-105 yum.repos.d]#


List all CM users

curl -u egruppioni:cloudera 'http://172.31.24.105:7180/api/v17/users'

[root@ip-172-31-24-105 yum.repos.d]# curl -u egruppioni:cloudera 'http://172.3124.105:7180/api/v17/users'
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "egruppioni",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}[root@ip-172-31-24-105 yum.repos.d]#


Report the database server in use by CM

curl -u egruppioni:cloudera 'http://172.31.24.105:7180/api/v17/cm/scmDbInfo'

[root@ip-172-31-24-105 yum.repos.d]# curl -u egruppioni:cloudera 'http://172.3124.105:7180/api/v17/cm/scmDbInfo'
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}[root@ip-172-31-24-105 yum.repos.d]#

```