{
  "timestamp" : "2018-05-16T18:14:30.669Z",
  "clusters" : [ {
    "name" : "Dzndrx",
    "version" : "CDH5",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "dataDir",
            "value" : "/var/lib/zk"
          }, {
            "name" : "dataLogDir",
            "value" : "/var/lib/zk"
          }, {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "637534208"
          } ]
        } ],
        "items" : [ {
          "name" : "enableSecurity",
          "value" : "true"
        }, {
          "name" : "zookeeper_datadir_autocreate",
          "value" : "true"
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "emop4ghfxixrxosbo15ddttg6"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-da573c4465e0856976bf7f4ed5d9ff04",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "3d1cea65-bc4f-41f3-ae0d-0a32200af466"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7pjv1m6n7mwevqfrd9cmj1rbo"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-f5a1247f105728e8caf9dc7a1c56f5fb",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "deabbf6a-076a-480b-a275-bc48aaf3522e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cexnbb5er9um7r23eoxszyk2e"
          }, {
            "name" : "serverId",
            "value" : "3"
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
            "value" : "ip-172-31-10-250.us-west-2.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "cloudera"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "scm"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "637534208"
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
        "name" : "oozie-OOZIE_SERVER-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "47tgkfczqok0ydpwh49mkrv1u"
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
          "value" : "ip-172-31-10-250.us-west-2.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "cloudera"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "database_user",
          "value" : "scm"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-8e478dcd04bcaf8f1512f36adc3e35de"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "HUE_LOAD_BALANCER",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8jlzdiaqbfq2vea1ip2vhpd6p"
          } ]
        }
      }, {
        "name" : "hue-HUE_SERVER-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ {
            "name" : "navmetadataserver_cmdb_password",
            "value" : "fe81ff44-fe0b-4079-bbdf-14e930c5ddb6"
          }, {
            "name" : "role_jceks_password",
            "value" : "3q26qe3ebbo31fvc0v8i0wwi6"
          }, {
            "name" : "secret_key",
            "value" : "N3EEn10Q0UhoIyvrV6rj5Xqh26FmX2"
          } ]
        }
      }, {
        "name" : "hue-KT_RENEWER-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "KT_RENEWER",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "eaky7jwlko03klgetvgli955d"
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
            "value" : "637534208"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3220069990"
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "400"
          }, {
            "name" : "rm_io_weight",
            "value" : "200"
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
            "value" : "/dfs/jne"
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
            "value" : "637534208"
          }, {
            "name" : "role_config_suppression_namenode_java_heapsize_minimum_validator",
            "value" : "true"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "637534208"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_encrypt_data_transfer_algorithm",
          "value" : "AES/CTR/NoPadding"
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "bzDTikDhPCBHy6J4HfX8JFdVHc2P8M"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "nuCmrb3kH163ds9UV8uOXJHbH4c5Se"
        }, {
          "name" : "hadoop_security_authentication",
          "value" : "kerberos"
        }, {
          "name" : "hadoop_security_authorization",
          "value" : "true"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "7R1dXIdKuLxkHyhXyPrHSHpONXLlom"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "20"
        }, {
          "name" : "service_config_suppression_hadoop_secure_web_ui",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-80316e4b64c9753b1b20a99eb8abbb84",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "499d256b-2fb1-417d-a55f-1976e3c1eb5a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cgthinwheqzajwmj5o0e7kqa1"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-da573c4465e0856976bf7f4ed5d9ff04",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "3d1cea65-bc4f-41f3-ae0d-0a32200af466"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "48ex2qxjedam7tebf6kcrtiol"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-efa4ae763b2105b7201cc16ec6249175",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "374f8aa6-1ab3-4a01-9b67-e91323518d19"
        },
        "config" : {
          "items" : [ {
            "name" : "role_health_suppression_data_node_heap_dump_directory_free_space",
            "value" : "true"
          }, {
            "name" : "role_health_suppression_data_node_log_directory_free_space",
            "value" : "true"
          }, {
            "name" : "role_health_suppression_datanode_data_directories_free_space",
            "value" : "true"
          }, {
            "name" : "role_jceks_password",
            "value" : "93ywoqrxrju1us1uxn5viwyx0"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-f5a1247f105728e8caf9dc7a1c56f5fb",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "deabbf6a-076a-480b-a275-bc48aaf3522e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c0l3uk4dttx67saugs40p0eks"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "25c1f67zss7ygtwrxpg2p9gl9"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-da573c4465e0856976bf7f4ed5d9ff04",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "3d1cea65-bc4f-41f3-ae0d-0a32200af466"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "61oai1toz61bufplc2birxh1a"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bfiyagrk72wz5ql28heill64y"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-da573c4465e0856976bf7f4ed5d9ff04",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "3d1cea65-bc4f-41f3-ae0d-0a32200af466"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cphpgcwtbezzqcgwuwr9ytodf"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-f5a1247f105728e8caf9dc7a1c56f5fb",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "deabbf6a-076a-480b-a275-bc48aaf3522e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "765qo5wf4beulrkznerddr0fu"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
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
            "value" : "48"
          }, {
            "name" : "role_jceks_password",
            "value" : "ajalaeybfl329amlazmudh2db"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-da573c4465e0856976bf7f4ed5d9ff04",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "3d1cea65-bc4f-41f3-ae0d-0a32200af466"
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
            "value" : "63"
          }, {
            "name" : "role_jceks_password",
            "value" : "1zwqv56a2tifxqv0f02zhv5mn"
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
            "value" : "3"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "637534208"
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
            "value" : "3370"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "637534208"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5949"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "80"
        }, {
          "name" : "service_config_suppression_hadoop_secure_web_ui",
          "value" : "true"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "WNNbRSmtF4fZSyJLfMJoZHdDGZfHoo"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d91h2sysskf9ak81rrvyps50d"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-80316e4b64c9753b1b20a99eb8abbb84",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "499d256b-2fb1-417d-a55f-1976e3c1eb5a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "xoaufcsw39b4jnnlq90rbgfr"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-da573c4465e0856976bf7f4ed5d9ff04",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "3d1cea65-bc4f-41f3-ae0d-0a32200af466"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3wrg1wx6m2srjzt3xvwp6rgw7"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-efa4ae763b2105b7201cc16ec6249175",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "374f8aa6-1ab3-4a01-9b67-e91323518d19"
        },
        "config" : {
          "items" : [ {
            "name" : "role_health_suppression_node_manager_heap_dump_directory_free_space",
            "value" : "true"
          }, {
            "name" : "role_health_suppression_node_manager_log_directory_free_space",
            "value" : "true"
          }, {
            "name" : "role_health_suppression_nodemanager_local_data_directories_free_space",
            "value" : "true"
          }, {
            "name" : "role_health_suppression_nodemanager_log_directories_free_space",
            "value" : "true"
          }, {
            "name" : "role_health_suppression_nodemanager_recovery_directory_free_space",
            "value" : "true"
          }, {
            "name" : "role_jceks_password",
            "value" : "bisdujpdtjlkhcriszmfelxn7"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-f5a1247f105728e8caf9dc7a1c56f5fb",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "deabbf6a-076a-480b-a275-bc48aaf3522e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5zridlm7rthtkal7vmxfd9tf0"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "55"
          }, {
            "name" : "role_jceks_password",
            "value" : "9xacwos353bmtdafams1u73pu"
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
            "name" : "hive_enable_db_notification",
            "value" : "true"
          }, {
            "name" : "hive_metastore_java_heapsize",
            "value" : "637534208"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_enable_impersonation",
            "value" : "false"
          }, {
            "name" : "hiveserver2_java_heapsize",
            "value" : "637534208"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "4115975372"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "692"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-10-250.us-west-2.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "sample"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "cloudera"
        }, {
          "name" : "hive_metastore_database_user",
          "value" : "scm"
        }, {
          "name" : "hive_proxy_user_groups_list",
          "value" : "hive,hue,sentry"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "sentry_service",
          "value" : "sentry"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-80316e4b64c9753b1b20a99eb8abbb84",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "499d256b-2fb1-417d-a55f-1976e3c1eb5a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-da573c4465e0856976bf7f4ed5d9ff04",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "3d1cea65-bc4f-41f3-ae0d-0a32200af466"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-efa4ae763b2105b7201cc16ec6249175",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "374f8aa6-1ab3-4a01-9b67-e91323518d19"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-f5a1247f105728e8caf9dc7a1c56f5fb",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "deabbf6a-076a-480b-a275-bc48aaf3522e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7u80g7g69agj43w1g2m0vfy9y"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-8e478dcd04bcaf8f1512f36adc3e35de",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bogn8m4q5ttezon9ms0p76t6v"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "sentry",
      "type" : "SENTRY",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SENTRY_SERVER",
          "items" : [ {
            "name" : "sentry_server_java_heapsize",
            "value" : "268435456"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "sentry_server_database_host",
          "value" : "ip-172-31-10-250.us-west-2.compute.internal"
        }, {
          "name" : "sentry_server_database_password",
          "value" : "cloudera"
        }, {
          "name" : "sentry_server_database_user",
          "value" : "scm"
        }, {
          "name" : "sentry_service_admin_group",
          "value" : "hive,impala,hue,solr,kafka,hbase,stest"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "sentry-SENTRY_SERVER-efa4ae763b2105b7201cc16ec6249175",
        "type" : "SENTRY_SERVER",
        "hostRef" : {
          "hostId" : "374f8aa6-1ab3-4a01-9b67-e91323518d19"
        },
        "config" : {
          "items" : [ {
            "name" : "role_health_suppression_sentry_server_heap_dump_directory_free_space",
            "value" : "true"
          }, {
            "name" : "role_health_suppression_sentry_server_log_directory_free_space",
            "value" : "true"
          }, {
            "name" : "role_jceks_password",
            "value" : "5isorrszr9nxq8jdhn6cyr4pu"
          } ]
        }
      } ],
      "displayName" : "Sentry"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "472c19a8-803b-4d69-815b-006a713d7525",
    "ipAddress" : "172.31.10.250",
    "hostname" : "ip-172-31-10-250.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ {
        "name" : "host_config_suppression_memory_overcommitted_validator",
        "value" : "true"
      } ]
    }
  }, {
    "hostId" : "3d1cea65-bc4f-41f3-ae0d-0a32200af466",
    "ipAddress" : "172.31.10.60",
    "hostname" : "ip-172-31-10-60.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "deabbf6a-076a-480b-a275-bc48aaf3522e",
    "ipAddress" : "172.31.13.119",
    "hostname" : "ip-172-31-13-119.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "374f8aa6-1ab3-4a01-9b67-e91323518d19",
    "ipAddress" : "172.31.4.194",
    "hostname" : "ip-172-31-4-194.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ {
        "name" : "host_config_suppression_memory_overcommitted_validator",
        "value" : "true"
      } ]
    }
  }, {
    "hostId" : "499d256b-2fb1-417d-a55f-1976e3c1eb5a",
    "ipAddress" : "172.31.6.94",
    "hostname" : "ip-172-31-6-94.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "Dzndrx",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "f3b5b5554865359d66c13c598c56a6e55dc564835f870af40992d7cf2331a8e3",
    "pwSalt" : -1781717535232266111,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__hue-HUE_SERVER-8e478dcd04bcaf8f1512f36adc3e35de",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ],
    "pwHash" : "0921dd2c615b59918cb7d09e5bb738e54354537dc8434fe749041d4e59b42345",
    "pwSalt" : -6916515163689849646,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-8e478dcd04bcaf8f1512f36adc3e35de",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "5c73088ef6b3bcb906db8bb145be32342378845123b5e2032575f633450e2d7e",
    "pwSalt" : 7107545251933321978,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-8e478dcd04bcaf8f1512f36adc3e35de",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "ec422c6ca39de79df14a1fd61386429ca5fcd95be8a2a1542f483079efc5161b",
    "pwSalt" : 4295664519250677569,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-8e478dcd04bcaf8f1512f36adc3e35de",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "fc54a4bca5b3325536ef8d1c691a3c3afb88654cde2cae51e637377c144430f3",
    "pwSalt" : 4609372080570121550,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-8e478dcd04bcaf8f1512f36adc3e35de",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "87494316fed236c1e778810d9cd083d207516786db909621f297d14e9584572b",
    "pwSalt" : 3996668140998958412,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "5adfb06fe1e180dd75f5a413cf7796c9cb4a5eb2e59088147da88faf9f579a4a",
    "pwSalt" : 5931257327117532846,
    "pwLogin" : true
  }, {
    "name" : "configMaster",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "bfc821b9c7b77df9f68a7674104cab4d44a830504708d2edc0acfa9dd58f8d76",
    "pwSalt" : 9078002631074066305,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.14.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20180414-0409",
    "gitHash" : "7f2725eea4edeb1d184a2888db790d332167b6f8",
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
          "value" : "637534208"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "637534208"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "828375040"
        }, {
          "name" : "role_config_suppression_firehose_host_monitor_heap_role_validator",
          "value" : "true"
        }, {
          "name" : "role_config_suppression_firehose_host_monitor_non_java_memory_role_validator",
          "value" : "true"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-10-250.us-west-2.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "scm"
        }, {
          "name" : "headlamp_database_password",
          "value" : "cloudera"
        }, {
          "name" : "headlamp_database_user",
          "value" : "scm"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "637534208"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "637534208"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "828375040"
        }, {
          "name" : "role_config_suppression_firehose_service_monitor_heap_role_validator",
          "value" : "true"
        }, {
          "name" : "role_config_suppression_firehose_service_monitor_non_java_memory_role_validator",
          "value" : "true"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-8e478dcd04bcaf8f1512f36adc3e35de",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "dr1z6628a0aq7gpn80fu98njg"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-8e478dcd04bcaf8f1512f36adc3e35de",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5bbhsonkrzntf68rexq6go6va"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-8e478dcd04bcaf8f1512f36adc3e35de",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "alwa26powkjof660vc0eqyelp"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-8e478dcd04bcaf8f1512f36adc3e35de",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "apcek1qnus5w35w7ojr810iav"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-8e478dcd04bcaf8f1512f36adc3e35de",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "472c19a8-803b-4d69-815b-006a713d7525"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "cghnl65tql7yj3jt6pzcm1pto"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "AD_USE_SIMPLE_AUTH",
      "value" : "false"
    }, {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/25/2012 22:10"
    }, {
      "name" : "KDC_ADMIN_HOST",
      "value" : "ip-172-31-10-250.us-west-2.compute.internal"
    }, {
      "name" : "KDC_ADMIN_PASSWORD",
      "value" : "BQIAAABFAAIAC0VYQU1QTEUuQ09NAAxjbG91ZGVyYS1zY20ABWFkbWluAAAAAVr8CxQBABcAEK866MWheIaXBLYvJrLwXY0AAAAB"
    }, {
      "name" : "KDC_ADMIN_USER",
      "value" : "cloudera-scm/admin@EXAMPLE.COM"
    }, {
      "name" : "KDC_HOST",
      "value" : "ip-172-31-10-250.us-west-2.compute.internal"
    }, {
      "name" : "KRB_MANAGE_KRB5_CONF",
      "value" : "true"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    }, {
      "name" : "SECURITY_REALM",
      "value" : "EXAMPLE.COM"
    } ]
  }
