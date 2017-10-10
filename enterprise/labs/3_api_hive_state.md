Stop Hive

```
curl -X POST -u egruppioni:cloudera 'http://172.31.24.105:7180/api/v12/clusters/cluster/services/hive/commands/stop'
```

```
{
  "id" : 191,
  "name" : "Stop",
  "startTime" : "2017-10-10T15:01:44.019Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```

Start Hive

```
curl -X POST -u egruppioni:cloudera 'http://172.31.24.105:7180/api/v12/clusters/cluster/services/hive/commands/start'
```

```
{
  "id" : 195,
  "name" : "Start",
  "startTime" : "2017-10-10T15:04:30.069Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```

Hive Status

```
curl -u egruppioni:cloudera 'http://172.31.24.105:7180/api/v12/clusters/cluster/services/hive'
```

```
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-24-105.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-24-105.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
}
```