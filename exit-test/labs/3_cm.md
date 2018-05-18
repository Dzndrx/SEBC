# HDFS LS 
[hdfs@ip-172-31-14-245 sometinh]$ hdfs dfs -ls /user
Found 7 items
drwxr-xr-x   - hdfs   supergroup          0 2018-05-18 05:30 /user/groot
drwxrwxrwx   - mapred hadoop              0 2018-05-18 05:25 /user/history
drwxrwxr-t   - hive   hive                0 2018-05-18 05:25 /user/hive
drwxrwxr-x   - hue    hue                 0 2018-05-18 05:26 /user/hue
drwxr-xr-x   - hdfs   supergroup          0 2018-05-18 05:30 /user/hulk
drwxrwxr-x   - oozie  oozie               0 2018-05-18 05:26 /user/oozie
drwxr-xr-x   - hdfs   supergroup          0 2018-05-18 05:30 /user/thanos


# API CALLS
[hdfs@ip-172-31-14-245 sometinh]$ curl -X GET -u admin:admin http://ip-172-31-14                                                                                        -245:7180/api/v5/hosts
{
  "items" : [ {
    "hostId" : "007bd120-582b-4aa4-899d-edd75434e023",
    "ipAddress" : "172.31.0.110",
    "hostname" : "ip-172-31-0-110.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:7180/cmf/hos                                                                                        tRedirect/007bd120-582b-4aa4-899d-edd75434e023",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 16656265216
  }, {
    "hostId" : "9c1bc14e-a9a7-48b0-8a31-81c0a75118d2",
    "ipAddress" : "172.31.14.245",
    "hostname" : "ip-172-31-14-245.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:7180/cmf/hos                                                                                        tRedirect/9c1bc14e-a9a7-48b0-8a31-81c0a75118d2",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 16656265216
  }, {
    "hostId" : "cafeb0fb-becf-481e-af5a-d1ea2d88f9ba",
    "ipAddress" : "172.31.15.59",
    "hostname" : "ip-172-31-15-59.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:7180/cmf/hos                                                                                        tRedirect/cafeb0fb-becf-481e-af5a-d1ea2d88f9ba",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 16656269312
  }, {
    "hostId" : "8b1a6823-edb6-4140-9156-70830c67d256",
    "ipAddress" : "172.31.2.224",
    "hostname" : "ip-172-31-2-224.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:7180/cmf/hos                                                                                        tRedirect/8b1a6823-edb6-4140-9156-70830c67d256",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 16656269312
  }, {
    "hostId" : "b0679647-0600-48ad-9b8d-949c383a7430",
    "ipAddress" : "172.31.5.78",
    "hostname" : "ip-172-31-5-78.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:7180/cmf/hos                                                                                        tRedirect/b0679647-0600-48ad-9b8d-949c383a7430",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 16656269312
  } ]


#hdfs@ip-172-31-14-245 sometinh]$ curl -X GET -u admin:admin http://ip-172-31-14                                                                                        -245:7180/api/v11/clusters/Dzndrx/services
{
  "items" : [ {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:7180/cmf/                                                                                        serviceRedirect/zookeeper",
    "roleInstancesUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:718                                                                                        0/cmf/serviceRedirect/zookeeper/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:7180/cmf/                                                                                        serviceRedirect/oozie",
    "roleInstancesUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:718                                                                                        0/cmf/serviceRedirect/oozie/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:7180/cmf/                                                                                        serviceRedirect/hue",
    "roleInstancesUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:718                                                                                        0/cmf/serviceRedirect/hue/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:7180/cmf/                                                                                        serviceRedirect/hdfs",
    "roleInstancesUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:718                                                                                        0/cmf/serviceRedirect/hdfs/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:7180/cmf/                                                                                        serviceRedirect/yarn",
    "roleInstancesUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:718                                                                                        0/cmf/serviceRedirect/yarn/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hbase",
    "type" : "HBASE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:7180/cmf/                                                                                        serviceRedirect/hbase",
    "roleInstancesUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:718                                                                                        0/cmf/serviceRedirect/hbase/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HBASE_MASTER_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HBASE_REGION_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HBase",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:7180/cmf/                                                                                        serviceRedirect/hive",
    "roleInstancesUrl" : "http://ip-172-31-14-245.us-west-2.compute.internal:718                                                                                        0/cmf/serviceRedirect/hive/instances",
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
  } ]
