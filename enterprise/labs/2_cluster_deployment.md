```
[root@ip-172-31-24-105 ~]# curl -X GET -u "egruppioni:cloudera" -i  http://172.31.24.105:7180/api/v2/cm/deployment
HTTP/1.1 200 OK
Expires: Thu, 01-Jan-1970 00:00:00 GMT
Set-Cookie: CLOUDERA_MANAGER_SESSIONID=m77sxfy8w73y1eqk206nr0rhv;Path=/;HttpOnly
Content-Type: application/json
Date: Tue, 10 Oct 2017 14:56:45 GMT
Transfer-Encoding: chunked
Server: Jetty(6.1.26.cloudera.4)

{
  "timestamp" : "2017-10-10T14:56:45.334Z",
  "clusters" : [ {
    "name" : "egruppioni",
    "version" : "CDH5",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "609222656"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-a03e837a214f0236bdd636ae76856a0d",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cne4bedjzdfz4tu0jr9aq2phy"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-a7c46939942ce0f718bff891733947c0",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "24aefa2a-2a50-490a-85d1-83b48cd071fb"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "45mllpwil6b2dhuh2w9n0vtvm"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-fb9a37285d9d4d000a336eb00a408ade",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "db2eb1c0-d31f-41e1-8588-3b32d7a5bb34"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bqg83c6hbf9e3zxryiny73wd8"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-24-105.eu-central-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "password"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "609222656"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-a03e837a214f0236bdd636ae76856a0d",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "16xr63my3ckt6okxk7ajkm877"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-24-105.eu-central-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "password"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-a03e837a214f0236bdd636ae76856a0d"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-a03e837a214f0236bdd636ae76856a0d",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "f5cw0ne14u7kp1ioh2e40pp1g"
          }, {
            "name" : "secret_key",
            "value" : "A4tTLOqo8htDky055vbzRd2B8xdWz5"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "609222656"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3157155020"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "609222656"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "609222656"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "uqC6D4W9oeZBjzPbrh8rElgsSObsJF"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "oL8EcSwK9zlXnlLujaGl1U6H6CgqaO"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "fGWilOVBr1r50qQWXeZD3w93LQLi6T"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-a03e837a214f0236bdd636ae76856a0d",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-2c3460c37a176c27826db96d542993ac",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "ef917865-0575-42f1-8b06-be50d94d8ee8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2ka93vecvu1xdtqjp8ld6xa9s"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-a7c46939942ce0f718bff891733947c0",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "24aefa2a-2a50-490a-85d1-83b48cd071fb"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4hfgj3sp5nbqbzrp6wuzobr5e"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-da500282cccdabd7f3862e83ab35cf25",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "0a254e64-8702-4ad4-82b8-6bf7e02fc60f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cp0w8bsc3u7p4t3d9momhgoqf"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-fb9a37285d9d4d000a336eb00a408ade",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "db2eb1c0-d31f-41e1-8588-3b32d7a5bb34"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d12t542yz1b4f3tbmd9aotyt3"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-a03e837a214f0236bdd636ae76856a0d",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2zd5pcdmc7nrr329axkfdfls5"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-fb9a37285d9d4d000a336eb00a408ade",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "db2eb1c0-d31f-41e1-8588-3b32d7a5bb34"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3088ozlcy05zc0taabu0qzw4n"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-2c3460c37a176c27826db96d542993ac",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "ef917865-0575-42f1-8b06-be50d94d8ee8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "duu2vzv70v39au2nd3eivxap2"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-a7c46939942ce0f718bff891733947c0",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "24aefa2a-2a50-490a-85d1-83b48cd071fb"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6yjfz1roxw8bmuzq00gyxrysq"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-da500282cccdabd7f3862e83ab35cf25",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "0a254e64-8702-4ad4-82b8-6bf7e02fc60f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3w6517r8wor0z7ue3bl9mrcj"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-a03e837a214f0236bdd636ae76856a0d",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "46"
          }, {
            "name" : "role_jceks_password",
            "value" : "94ekrc3h4ml9y9kcur6b76qzv"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-fb9a37285d9d4d000a336eb00a408ade",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "db2eb1c0-d31f-41e1-8588-3b32d7a5bb34"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "61"
          }, {
            "name" : "role_jceks_password",
            "value" : "7e29j5u2q8x8qv9sel76hyzcw"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "8"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "609222656"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "5192"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "609222656"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5192"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "4"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "4pz6MmmVSAonexglyK6yrVsmFfyUM6"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-a03e837a214f0236bdd636ae76856a0d",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4beh93ineo5xawttddoxsfiq7"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-2c3460c37a176c27826db96d542993ac",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "ef917865-0575-42f1-8b06-be50d94d8ee8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "63zzhgl4f8o6a83fdp3sognsx"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-a7c46939942ce0f718bff891733947c0",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "24aefa2a-2a50-490a-85d1-83b48cd071fb"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4pql8minxi3hdjmph4fa7rzp5"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-da500282cccdabd7f3862e83ab35cf25",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "0a254e64-8702-4ad4-82b8-6bf7e02fc60f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6v779y7e3erwqwpop9gwr75xw"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-fb9a37285d9d4d000a336eb00a408ade",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "db2eb1c0-d31f-41e1-8588-3b32d7a5bb34"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2n0mabiv4jjgd9gulv7su5odt"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-a03e837a214f0236bdd636ae76856a0d",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "53"
          }, {
            "name" : "role_jceks_password",
            "value" : "f0nrg3ycec2pthbwnt4gvfjl6"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "609222656"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "609222656"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "3545550028"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "596"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-24-105.eu-central-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "password"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-2c3460c37a176c27826db96d542993ac",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "ef917865-0575-42f1-8b06-be50d94d8ee8"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-a03e837a214f0236bdd636ae76856a0d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-a7c46939942ce0f718bff891733947c0",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "24aefa2a-2a50-490a-85d1-83b48cd071fb"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-da500282cccdabd7f3862e83ab35cf25",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "0a254e64-8702-4ad4-82b8-6bf7e02fc60f"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-fb9a37285d9d4d000a336eb00a408ade",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "db2eb1c0-d31f-41e1-8588-3b32d7a5bb34"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-a03e837a214f0236bdd636ae76856a0d",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8ug6besuvrd4jyyqthe5vs8mf"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-a03e837a214f0236bdd636ae76856a0d",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bua7qwxfmjplm833ispk5hrrx"
          } ]
        }
      } ],
      "displayName" : "Hive"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0",
    "ipAddress" : "172.31.18.42",
    "hostname" : "ip-172-31-18-42.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "db2eb1c0-d31f-41e1-8588-3b32d7a5bb34",
    "ipAddress" : "172.31.20.187",
    "hostname" : "ip-172-31-20-187.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "24aefa2a-2a50-490a-85d1-83b48cd071fb",
    "ipAddress" : "172.31.24.105",
    "hostname" : "ip-172-31-24-105.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "0a254e64-8702-4ad4-82b8-6bf7e02fc60f",
    "ipAddress" : "172.31.26.219",
    "hostname" : "ip-172-31-26-219.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "ef917865-0575-42f1-8b06-be50d94d8ee8",
    "ipAddress" : "172.31.30.118",
    "hostname" : "ip-172-31-30-118.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-a03e837a214f0236bdd636ae76856a0d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "991249e406300071aa8838dc797fb040afec056a49722cf177710c1a5296616a",
    "pwSalt" : -8976308967144220578,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-a03e837a214f0236bdd636ae76856a0d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "75d99e412b30899ec513063d58eb7e90d82597e6049d316e5e00152867399778",
    "pwSalt" : 2117235002485289618,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-a03e837a214f0236bdd636ae76856a0d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "caef1cffa29a73784c69c18ab0c5c0d3c9ae5bee51bc84e0330870deeb974856",
    "pwSalt" : -2027302042902921165,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-a03e837a214f0236bdd636ae76856a0d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "c90d5ee27791ee9c8c85888515422e289dce4c42a2f5a8d1703acb126c446681",
    "pwSalt" : -2938273612503244283,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "a2fd6f04c3b0cde9cb29b02e2d4f27038b8a3d3f16d7dd47fa750113258d61cc",
    "pwSalt" : 1086278412828096519,
    "pwLogin" : true
  }, {
    "name" : "egruppioni",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "8407548ae98fdceb7e42e67056da726a54c6ce0c1cb639221bb66f37fc575303",
    "pwSalt" : 4696421480795945776,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "0f17bb8bf2e5a58bab6995412272fe0ca535d2025a18c7237c84e641e80f62d2",
    "pwSalt" : -8342495502058286278,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.11.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170811-0014",
    "gitHash" : "3c3ea33a12076fb83a8f11c4452c52fac685d01b",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "609222656"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "609222656"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-24-105.eu-central-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "password"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "609222656"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "609222656"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-a03e837a214f0236bdd636ae76856a0d",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4sggyrrq5czii1ggbd7f9r9i"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-a03e837a214f0236bdd636ae76856a0d",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "699nkzaooxwj3n7ibsft7mc04"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-a03e837a214f0236bdd636ae76856a0d",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4430ymex1agf7l52yvj4ikvdp"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-a03e837a214f0236bdd636ae76856a0d",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "eqmo2ibi26b820rxiioctykb6"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-a03e837a214f0236bdd636ae76856a0d",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "d6dfb0b3-e5b4-4631-a0c7-e1c4cbcff2d0"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "au0xuugnuo2njrtzxq1inz5sf"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/25/2012 23:50"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/5.10,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}

```