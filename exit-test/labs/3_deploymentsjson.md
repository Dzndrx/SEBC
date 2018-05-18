[hdfs@ip-172-31-14-245 sometinh]$ curl -X GET -u admin:admin http://ip-172-31-14                                                                                        -245:7180/api/v14/cm/deployment
{
  "timestamp" : "2018-05-18T05:36:25.216Z",
  "clusters" : [ {
    "name" : "cluster",
    "displayName" : "Dzndrx",
    "version" : "CDH5",
    "fullVersion" : "5.11.2",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-b1e5a9297ab8303a70b29a915f65886a",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1u5k81d7epj7b4902wab0jzb8",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "1",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      } ],
      "displayName" : "ZooKeeper",
      "roleConfigGroups" : [ {
        "name" : "zookeeper-SERVER-BASE",
        "displayName" : "Server Default Group",
        "roleType" : "SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "zookeeper"
        },
        "config" : {
          "items" : [ {
            "name" : "maxSessionTimeout",
            "value" : "60000",
            "sensitive" : false
          }, {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "609222656",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-b1e5a9297ab8303a70b29a915f65886a",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "abnwqp7wa7atdj46e78bzcez0",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "oozie-OOZIE_SERVER-BASE"
        }
      } ],
      "displayName" : "Oozie",
      "roleConfigGroups" : [ {
        "name" : "oozie-OOZIE_SERVER-BASE",
        "displayName" : "Oozie Server Default Group",
        "roleType" : "OOZIE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "oozie"
        },
        "config" : {
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-2-224.us-west-2.compute.internal",
            "sensitive" : false
          }, {
            "name" : "oozie_database_password",
            "value" : "elabrigo",
            "sensitive" : true
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql",
            "sensitive" : false
          }, {
            "name" : "oozie_database_user",
            "value" : "scmadmin",
            "sensitive" : false
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "609222656",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-2-224.us-west-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "database_password",
          "value" : "elabrigo",
          "sensitive" : true
        }, {
          "name" : "database_type",
          "value" : "mysql",
          "sensitive" : false
        }, {
          "name" : "database_user",
          "value" : "scmadmin",
          "sensitive" : false
        }, {
          "name" : "hbase_service",
          "value" : "hbase",
          "sensitive" : false
        }, {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-b1e5a9297ab8303a70b29a915f65886a",
          "sensitive" : false
        }, {
          "name" : "oozie_service",
          "value" : "oozie",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-b1e5a9297ab8303a70b29a915f65886a",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d457a54l45g2h10zqzgjkvzdx",
            "sensitive" : true
          }, {
            "name" : "secret_key",
            "value" : "bjvIk82ZcSEIP9aT4ya5jfnMPeZFKN",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_SERVER-BASE"
        }
      } ],
      "displayName" : "Hue",
      "roleConfigGroups" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-BASE",
        "displayName" : "Load Balancer Default Group",
        "roleType" : "HUE_LOAD_BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hue-HUE_SERVER-BASE",
        "displayName" : "Hue Server Default Group",
        "roleType" : "HUE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hue-KT_RENEWER-BASE",
        "displayName" : "Kerberos Ticket Renewer Default Group",
        "roleType" : "KT_RENEWER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "f8PuV1ZFBephsYBbcWgUgQoC7fQqzD",
          "sensitive" : true
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "2N8hugmrPDrqT5FdNglTnt5aWGS0nl",
          "sensitive" : true
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "X7DEhefgvLR8N31gt1JkiEAP7O8FEG",
          "sensitive" : true
        }, {
          "name" : "rm_dirty",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-b1e5a9297ab8303a70b29a915f65886a",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-BALANCER-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-61d97c283e355176ed68c47ad781b2fa",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "9c1bc14e-a9a7-48b0-8a31-81c0a75118d2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bkknwakc1y2mde509pl5fgn30",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-919afe68c26ee4c624a1001386bf5e85",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "8b1a6823-edb6-4140-9156-70830c67d256"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ag89d5ogomuz40fhvr68uzcml",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-c591a7930aaa8a5c36783d5c52b76166",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "007bd120-582b-4aa4-899d-edd75434e023"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "903mrixj935xbpzmgfg9gyo8x",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-f16af600e52862d2962e0430adecdab6",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "b0679647-0600-48ad-9b8d-949c383a7430"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "262p3ocui5bydz3563qbeg5ws",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-b1e5a9297ab8303a70b29a915f65886a",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "namenode_id",
            "value" : "47",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "ej731fj48lyohqnohv1eqgxkf",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-b1e5a9297ab8303a70b29a915f65886a",
        "type" : "SECONDARYNAMENODE",
        "hostRef" : {
          "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8dmedxsuwl3ldtyxtlw65jmdo",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-SECONDARYNAMENODE-BASE"
        }
      } ],
      "displayName" : "HDFS",
      "roleConfigGroups" : [ {
        "name" : "hdfs-BALANCER-BASE",
        "displayName" : "Balancer Default Group",
        "roleType" : "BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "609222656",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-BASE",
        "displayName" : "DataNode Default Group",
        "roleType" : "DATANODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "5367553638",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "3153068032",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-BASE",
        "displayName" : "Failover Controller Default Group",
        "roleType" : "FAILOVERCONTROLLER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-BASE",
        "displayName" : "HttpFS Default Group",
        "roleType" : "HTTPFS",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-BASE",
        "displayName" : "JournalNode Default Group",
        "roleType" : "JOURNALNODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-NAMENODE-BASE",
        "displayName" : "NameNode Default Group",
        "roleType" : "NAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022",
            "sensitive" : false
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "609222656",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-BASE",
        "displayName" : "NFS Gateway Default Group",
        "roleType" : "NFSGATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-BASE",
        "displayName" : "SecondaryNameNode Default Group",
        "roleType" : "SECONDARYNAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn",
            "sensitive" : false
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "609222656",
            "sensitive" : false
          } ]
        }
      } ],
      "replicationSchedules" : [ ],
      "snapshotPolicies" : [ ]
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs",
          "sensitive" : false
        }, {
          "name" : "rm_dirty",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "pWF3RXLuEYoEMtpIisFRtlGoJf1oTT",
          "sensitive" : true
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-b1e5a9297ab8303a70b29a915f65886a",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ai54maf7wflq1jkq9d1ww1lrr",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-JOBHISTORY-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-61d97c283e355176ed68c47ad781b2fa",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "9c1bc14e-a9a7-48b0-8a31-81c0a75118d2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3ktxwdmwwq51fglnuqpe1vdec",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-919afe68c26ee4c624a1001386bf5e85",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "8b1a6823-edb6-4140-9156-70830c67d256"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bnl05qgnpouswpl8q71earhud",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-c591a7930aaa8a5c36783d5c52b76166",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "007bd120-582b-4aa4-899d-edd75434e023"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1bbhb6rxwb1fe1z8veepo76oo",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-f16af600e52862d2962e0430adecdab6",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "b0679647-0600-48ad-9b8d-949c383a7430"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8pxdntu48mnrzpkoh4iczxiyr",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-b1e5a9297ab8303a70b29a915f65886a",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "54",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "ajwiysn89qavvwu9io784lars",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-RESOURCEMANAGER-BASE"
        }
      } ],
      "displayName" : "YARN (MR2 Included)",
      "roleConfigGroups" : [ {
        "name" : "yarn-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "8",
            "sensitive" : false
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-BASE",
        "displayName" : "JobHistory Server Default Group",
        "roleType" : "JOBHISTORY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "609222656",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-BASE",
        "displayName" : "NodeManager Default Group",
        "roleType" : "NODEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "3007",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-BASE",
        "displayName" : "ResourceManager Default Group",
        "roleType" : "RESOURCEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "609222656",
            "sensitive" : false
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "3007",
            "sensitive" : false
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "4",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "hbase",
      "type" : "HBASE",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs",
          "sensitive" : false
        }, {
          "name" : "rm_dirty",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hbase-MASTER-b1e5a9297ab8303a70b29a915f65886a",
        "type" : "MASTER",
        "hostRef" : {
          "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "btsrig471dedpqotjgklz9mvm",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hbase-MASTER-BASE"
        }
      }, {
        "name" : "hbase-REGIONSERVER-61d97c283e355176ed68c47ad781b2fa",
        "type" : "REGIONSERVER",
        "hostRef" : {
          "hostId" : "9c1bc14e-a9a7-48b0-8a31-81c0a75118d2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1tfuqqz9kqxjo4dzkxekv4u2e",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hbase-REGIONSERVER-BASE"
        }
      }, {
        "name" : "hbase-REGIONSERVER-919afe68c26ee4c624a1001386bf5e85",
        "type" : "REGIONSERVER",
        "hostRef" : {
          "hostId" : "8b1a6823-edb6-4140-9156-70830c67d256"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "73ues3e5816qnnahk8tajrabn",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hbase-REGIONSERVER-BASE"
        }
      }, {
        "name" : "hbase-REGIONSERVER-c591a7930aaa8a5c36783d5c52b76166",
        "type" : "REGIONSERVER",
        "hostRef" : {
          "hostId" : "007bd120-582b-4aa4-899d-edd75434e023"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "56y1lw86xopeqn2c8g0dy3395",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hbase-REGIONSERVER-BASE"
        }
      }, {
        "name" : "hbase-REGIONSERVER-f16af600e52862d2962e0430adecdab6",
        "type" : "REGIONSERVER",
        "hostRef" : {
          "hostId" : "b0679647-0600-48ad-9b8d-949c383a7430"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "30xuoyzlugukmduf0sk26mt8i",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hbase-REGIONSERVER-BASE"
        }
      } ],
      "displayName" : "HBase",
      "roleConfigGroups" : [ {
        "name" : "hbase-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hbase"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hbase-HBASERESTSERVER-BASE",
        "displayName" : "HBase REST Server Default Group",
        "roleType" : "HBASERESTSERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hbase"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hbase-HBASETHRIFTSERVER-BASE",
        "displayName" : "HBase Thrift Server Default Group",
        "roleType" : "HBASETHRIFTSERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hbase"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hbase-MASTER-BASE",
        "displayName" : "Master Default Group",
        "roleType" : "MASTER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hbase"
        },
        "config" : {
          "items" : [ {
            "name" : "hbase_master_java_heapsize",
            "value" : "609222656",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hbase-REGIONSERVER-BASE",
        "displayName" : "RegionServer Default Group",
        "roleType" : "REGIONSERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hbase"
        },
        "config" : {
          "items" : [ {
            "name" : "hbase_regionserver_java_heapsize",
            "value" : "2425356288",
            "sensitive" : false
          } ]
        }
      } ],
      "snapshotPolicies" : [ ]
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "items" : [ {
          "name" : "hbase_service",
          "value" : "hbase",
          "sensitive" : false
        }, {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-2-224.us-west-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "elabrigo",
          "sensitive" : true
        }, {
          "name" : "hive_metastore_database_user",
          "value" : "scmadmin",
          "sensitive" : false
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-61d97c283e355176ed68c47ad781b2fa",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "9c1bc14e-a9a7-48b0-8a31-81c0a75118d2"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-919afe68c26ee4c624a1001386bf5e85",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "8b1a6823-edb6-4140-9156-70830c67d256"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-b1e5a9297ab8303a70b29a915f65886a",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-c591a7930aaa8a5c36783d5c52b76166",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "007bd120-582b-4aa4-899d-edd75434e023"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-f16af600e52862d2962e0430adecdab6",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "b0679647-0600-48ad-9b8d-949c383a7430"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-HIVEMETASTORE-b1e5a9297ab8303a70b29a915f65886a",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3zjjvau44u21wg3awx668viwh",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVEMETASTORE-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-b1e5a9297ab8303a70b29a915f65886a",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ax0jpj0mhhycllld9a84cm8a5",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVESERVER2-BASE"
        }
      } ],
      "displayName" : "Hive",
      "roleConfigGroups" : [ {
        "name" : "hive-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-BASE",
        "displayName" : "Hive Metastore Server Default Group",
        "roleType" : "HIVEMETASTORE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "609222656",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-BASE",
        "displayName" : "HiveServer2 Default Group",
        "roleType" : "HIVESERVER2",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "609222656",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2680107827",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "451",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hive-WEBHCAT-BASE",
        "displayName" : "WebHCat Server Default Group",
        "roleType" : "WEBHCAT",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      } ],
      "replicationSchedules" : [ ]
    } ],
    "parcels" : [ {
      "product" : "CDH",
      "version" : "5.11.2-1.cdh5.11.2.p0.4",
      "stage" : "DISTRIBUTED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    }, {
      "product" : "CDH",
      "version" : "5.11.2-1.cdh5.11.2.p0.4",
      "stage" : "ACTIVATED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "007bd120-582b-4aa4-899d-edd75434e023",
    "ipAddress" : "172.31.0.110",
    "hostname" : "ip-172-31-0-110.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "9c1bc14e-a9a7-48b0-8a31-81c0a75118d2",
    "ipAddress" : "172.31.14.245",
    "hostname" : "ip-172-31-14-245.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba",
    "ipAddress" : "172.31.15.59",
    "hostname" : "ip-172-31-15-59.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "8b1a6823-edb6-4140-9156-70830c67d256",
    "ipAddress" : "172.31.2.224",
    "hostname" : "ip-172-31-2-224.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "b0679647-0600-48ad-9b8d-949c383a7430",
    "ipAddress" : "172.31.5.78",
    "hostname" : "ip-172-31-5-78.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-b1e5a9297ab8303a70b29a9                                                                                        15f65886a",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "e71af13f652b35faa64a249a625eaeefc49db3bdb0e2ef9dbc06be813f5c86cd                                                                                        ",
    "pwSalt" : 1036183732600054058,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-b1e5a9297ab8303a70b29a9                                                                                        15f65886a",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b4af23c46185210636f5b47f84960c8fc8267b03e5628ffc47f79609207c917a                                                                                        ",
    "pwSalt" : 2840718911590256825,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-b1e5a9297ab8303a70b2                                                                                        9a915f65886a",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "6b0c1434d6f428a13c4273bb34621cb74411d3017e9a9b82dfb9c47580ca7872                                                                                        ",
    "pwSalt" : -3011581741994670602,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-b1e5a9297ab8303a70b2                                                                                        9a915f65886a",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "07ba3c2fd3fa08ad7792c5529230b13a770cee7cbd038f0ae4482cec04b8441b                                                                                        ",
    "pwSalt" : -3749040201894600458,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "ec303ec89fc53057375d52e7346bcc41996c2e82d03bf084cd6de125ef624a28                                                                                        ",
    "pwSalt" : 1766314815760671837,
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
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-b1e5a9297ab8303a70b29a915f65886a",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5mvpkk2r5wildpr0kr9lh9438",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ALERTPUBLISHER-BASE"
      }
    }, {
      "name" : "mgmt-EVENTSERVER-b1e5a9297ab8303a70b29a915f65886a",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "cpmtw7b7l70uy9krzcwy74l3w",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-EVENTSERVER-BASE"
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-b1e5a9297ab8303a70b29a915f65886a",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7b23rlgr595gimxzeoxxuel8s",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-HOSTMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-b1e5a9297ab8303a70b29a915f65886a",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "3zksuayidz2nn9qxhzqgfkkt4",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-REPORTSMANAGER-BASE"
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-b1e5a9297ab8303a70b29a915f65886a",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "ab7w6auv50qsgfmlfvdofteeg",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-SERVICEMONITOR-BASE"
      }
    } ],
    "displayName" : "Cloudera Management Service",
    "roleConfigGroups" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-BASE",
      "displayName" : "Activity Monitor Default Group",
      "roleType" : "ACTIVITYMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-BASE",
      "displayName" : "Alert Publisher Default Group",
      "roleType" : "ALERTPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-BASE",
      "displayName" : "Event Server Default Group",
      "roleType" : "EVENTSERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "609222656",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-BASE",
      "displayName" : "Host Monitor Default Group",
      "roleType" : "HOSTMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "609222656",
          "sensitive" : false
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-NAVIGATOR-BASE",
      "displayName" : "Navigator Audit Server Default Group",
      "roleType" : "NAVIGATOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-NAVIGATORMETASERVER-BASE",
      "displayName" : "Navigator Metadata Server Default Group",
      "roleType" : "NAVIGATORMETASERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-BASE",
      "displayName" : "Reports Manager Default Group",
      "roleType" : "REPORTSMANAGER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-2-224.us-west-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman",
          "sensitive" : false
        }, {
          "name" : "headlamp_database_password",
          "value" : "elabrigo",
          "sensitive" : true
        }, {
          "name" : "headlamp_database_user",
          "value" : "scmadmin",
          "sensitive" : false
        }, {
          "name" : "headlamp_heapsize",
          "value" : "609222656",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-BASE",
      "displayName" : "Service Monitor Default Group",
      "roleType" : "SERVICEMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "609222656",
          "sensitive" : false
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-TELEMETRYPUBLISHER-BASE",
      "displayName" : "Telemetry Publisher Default Group",
      "roleType" : "TELEMETRYPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    } ]
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/22/2012 1:10",
      "sensitive" : false
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD",
      "sensitive" : false
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "http://ip-172-31-14-245.us-west-2.compute.internal/sometinh",
      "sensitive" : false
    } ]
  },
  "allHostsConfig" : {
    "items" : [ ]
  },
  "peers" : [ ],
  "hostTemplates" : {
    "items" : [ ]
  }
