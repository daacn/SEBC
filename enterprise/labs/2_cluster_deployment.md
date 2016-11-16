```JSON
{
  "timestamp": "2016-11-16T10:41:43.353Z",
  "clusters": [
    {
      "name": "daarn",
      "version": "CDH5",
      "services": [
        {
          "name": "hive",
          "type": "HIVE",
          "config": {
            "roleTypeConfigs": [
              {
                "roleType": "HIVEMETASTORE",
                "items": [
                  {
                    "name": "hive_metastore_java_heapsize",
                    "value": "593494016"
                  }
                ]
              },
              {
                "roleType": "HIVESERVER2",
                "items": [
                  {
                    "name": "hiveserver2_java_heapsize",
                    "value": "593494016"
                  },
                  {
                    "name": "hiveserver2_spark_driver_memory",
                    "value": "966367641"
                  },
                  {
                    "name": "hiveserver2_spark_executor_cores",
                    "value": "4"
                  },
                  {
                    "name": "hiveserver2_spark_executor_memory",
                    "value": "3433247539"
                  },
                  {
                    "name": "hiveserver2_spark_yarn_driver_memory_overhead",
                    "value": "102"
                  },
                  {
                    "name": "hiveserver2_spark_yarn_executor_memory_overhead",
                    "value": "577"
                  }
                ]
              }
            ],
            "items": [
              {
                "name": "hive_metastore_database_host",
                "value": "ip-172-31-50-73.ec2.internal"
              },
              {
                "name": "hive_metastore_database_password",
                "value": "password"
              },
              {
                "name": "hive_metastore_database_user",
                "value": "metastore"
              },
              {
                "name": "mapreduce_yarn_service",
                "value": "yarn"
              },
              {
                "name": "zookeeper_service",
                "value": "zookeeper"
              }
            ]
          },
          "roles": [
            {
              "name": "hive-GATEWAY-6b9563b4ee2e8483d8b994c73f15e46a",
              "type": "GATEWAY",
              "hostRef": {
                "hostId": "i-a3007dad"
              },
              "config": {
                "items": []
              }
            },
            {
              "name": "hive-GATEWAY-8691fd757828375a41864f9ab0ce2cd4",
              "type": "GATEWAY",
              "hostRef": {
                "hostId": "i-03ff8d0d"
              },
              "config": {
                "items": []
              }
            },
            {
              "name": "hive-GATEWAY-a8d991003cb9a7b756adf029e4c6d220",
              "type": "GATEWAY",
              "hostRef": {
                "hostId": "i-a0007dae"
              },
              "config": {
                "items": []
              }
            },
            {
              "name": "hive-GATEWAY-ae9f629b2be1b2161a198e7af1d74e66",
              "type": "GATEWAY",
              "hostRef": {
                "hostId": "i-a1007daf"
              },
              "config": {
                "items": []
              }
            },
            {
              "name": "hive-GATEWAY-d8c2c1bda620c2c5efe85ae4915ad489",
              "type": "GATEWAY",
              "hostRef": {
                "hostId": "i-cca3d1c2"
              },
              "config": {
                "items": []
              }
            },
            {
              "name": "hive-HIVEMETASTORE-8691fd757828375a41864f9ab0ce2cd4",
              "type": "HIVEMETASTORE",
              "hostRef": {
                "hostId": "i-03ff8d0d"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "3m8f5o7hxso9lahmaluenvz75"
                  }
                ]
              }
            },
            {
              "name": "hive-HIVESERVER2-8691fd757828375a41864f9ab0ce2cd4",
              "type": "HIVESERVER2",
              "hostRef": {
                "hostId": "i-03ff8d0d"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "2jep8f7zitzqlmoayd6y26y14"
                  }
                ]
              }
            }
          ],
          "displayName": "Hive"
        },
        {
          "name": "zookeeper",
          "type": "ZOOKEEPER",
          "config": {
            "roleTypeConfigs": [
              {
                "roleType": "SERVER",
                "items": [
                  {
                    "name": "zookeeper_server_java_heapsize",
                    "value": "593494016"
                  }
                ]
              }
            ],
            "items": []
          },
          "roles": [
            {
              "name": "zookeeper-SERVER-6b9563b4ee2e8483d8b994c73f15e46a",
              "type": "SERVER",
              "hostRef": {
                "hostId": "i-a3007dad"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "43r10r2fb96l8go4rzfszr4t9"
                  },
                  {
                    "name": "serverId",
                    "value": "2"
                  }
                ]
              }
            },
            {
              "name": "zookeeper-SERVER-8691fd757828375a41864f9ab0ce2cd4",
              "type": "SERVER",
              "hostRef": {
                "hostId": "i-03ff8d0d"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "e41gxg6f1qe0x8j3p8hmn0vme"
                  },
                  {
                    "name": "serverId",
                    "value": "3"
                  }
                ]
              }
            },
            {
              "name": "zookeeper-SERVER-d8c2c1bda620c2c5efe85ae4915ad489",
              "type": "SERVER",
              "hostRef": {
                "hostId": "i-cca3d1c2"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "c1jmtcffchehn7re07fw1k567"
                  },
                  {
                    "name": "serverId",
                    "value": "1"
                  }
                ]
              }
            }
          ],
          "displayName": "ZooKeeper"
        },
        {
          "name": "hue",
          "type": "HUE",
          "config": {
            "roleTypeConfigs": [],
            "items": [
              {
                "name": "database_host",
                "value": "ip-172-31-50-73.ec2.internal"
              },
              {
                "name": "database_password",
                "value": "password"
              },
              {
                "name": "database_type",
                "value": "mysql"
              },
              {
                "name": "hive_service",
                "value": "hive"
              },
              {
                "name": "hue_webhdfs",
                "value": "hdfs-NAMENODE-8691fd757828375a41864f9ab0ce2cd4"
              },
              {
                "name": "oozie_service",
                "value": "oozie"
              },
              {
                "name": "zookeeper_service",
                "value": "zookeeper"
              }
            ]
          },
          "roles": [
            {
              "name": "hue-HUE_SERVER-8691fd757828375a41864f9ab0ce2cd4",
              "type": "HUE_SERVER",
              "hostRef": {
                "hostId": "i-03ff8d0d"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "3no0aqnnc8x6xzd2perqjz45c"
                  },
                  {
                    "name": "secret_key",
                    "value": "pZyoJgqwieVeNxCvprwOGaE4t1cK5y"
                  }
                ]
              }
            }
          ],
          "displayName": "Hue"
        },
        {
          "name": "oozie",
          "type": "OOZIE",
          "config": {
            "roleTypeConfigs": [
              {
                "roleType": "OOZIE_SERVER",
                "items": [
                  {
                    "name": "oozie_database_host",
                    "value": "ip-172-31-50-73.ec2.internal"
                  },
                  {
                    "name": "oozie_database_password",
                    "value": "password"
                  },
                  {
                    "name": "oozie_database_type",
                    "value": "mysql"
                  },
                  {
                    "name": "oozie_database_user",
                    "value": "oozie"
                  },
                  {
                    "name": "oozie_java_heapsize",
                    "value": "593494016"
                  }
                ]
              }
            ],
            "items": [
              {
                "name": "hive_service",
                "value": "hive"
              },
              {
                "name": "mapreduce_yarn_service",
                "value": "yarn"
              },
              {
                "name": "zookeeper_service",
                "value": "zookeeper"
              }
            ]
          },
          "roles": [
            {
              "name": "oozie-OOZIE_SERVER-8691fd757828375a41864f9ab0ce2cd4",
              "type": "OOZIE_SERVER",
              "hostRef": {
                "hostId": "i-03ff8d0d"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "3mejeb2g49uq1cxxcbtnype05"
                  }
                ]
              }
            }
          ],
          "displayName": "Oozie"
        },
        {
          "name": "yarn",
          "type": "YARN",
          "config": {
            "roleTypeConfigs": [
              {
                "roleType": "GATEWAY",
                "items": [
                  {
                    "name": "mapred_reduce_tasks",
                    "value": "8"
                  },
                  {
                    "name": "mapred_submit_replication",
                    "value": "2"
                  }
                ]
              },
              {
                "roleType": "JOBHISTORY",
                "items": [
                  {
                    "name": "mr2_jobhistory_java_heapsize",
                    "value": "593494016"
                  }
                ]
              },
              {
                "roleType": "NODEMANAGER",
                "items": [
                  {
                    "name": "yarn_nodemanager_heartbeat_interval_ms",
                    "value": "100"
                  },
                  {
                    "name": "yarn_nodemanager_local_dirs",
                    "value": "/yarn/nm"
                  },
                  {
                    "name": "yarn_nodemanager_log_dirs",
                    "value": "/yarn/container-logs"
                  },
                  {
                    "name": "yarn_nodemanager_resource_cpu_vcores",
                    "value": "4"
                  },
                  {
                    "name": "yarn_nodemanager_resource_memory_mb",
                    "value": "4939"
                  }
                ]
              },
              {
                "roleType": "RESOURCEMANAGER",
                "items": [
                  {
                    "name": "resource_manager_java_heapsize",
                    "value": "593494016"
                  },
                  {
                    "name": "yarn_scheduler_maximum_allocation_mb",
                    "value": "4939"
                  },
                  {
                    "name": "yarn_scheduler_maximum_allocation_vcores",
                    "value": "4"
                  }
                ]
              }
            ],
            "items": [
              {
                "name": "hdfs_service",
                "value": "hdfs"
              },
              {
                "name": "rm_dirty",
                "value": "true"
              },
              {
                "name": "zk_authorization_secret_key",
                "value": "xEA0SDECf2FHwbV8s9jIV6CiOT6kwt"
              },
              {
                "name": "zookeeper_service",
                "value": "zookeeper"
              }
            ]
          },
          "roles": [
            {
              "name": "yarn-JOBHISTORY-8691fd757828375a41864f9ab0ce2cd4",
              "type": "JOBHISTORY",
              "hostRef": {
                "hostId": "i-03ff8d0d"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "cmmkfmbrol5n7kq3fejqubapx"
                  }
                ]
              }
            },
            {
              "name": "yarn-NODEMANAGER-6b9563b4ee2e8483d8b994c73f15e46a",
              "type": "NODEMANAGER",
              "hostRef": {
                "hostId": "i-a3007dad"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "1fmgvwfbf5667rdpvcd7yygo5"
                  }
                ]
              }
            },
            {
              "name": "yarn-NODEMANAGER-a8d991003cb9a7b756adf029e4c6d220",
              "type": "NODEMANAGER",
              "hostRef": {
                "hostId": "i-a0007dae"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "11tyzw6ydna7majmilnv01usj"
                  }
                ]
              }
            },
            {
              "name": "yarn-NODEMANAGER-ae9f629b2be1b2161a198e7af1d74e66",
              "type": "NODEMANAGER",
              "hostRef": {
                "hostId": "i-a1007daf"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "4h874ksymx09hwgekzs56a6vz"
                  }
                ]
              }
            },
            {
              "name": "yarn-NODEMANAGER-d8c2c1bda620c2c5efe85ae4915ad489",
              "type": "NODEMANAGER",
              "hostRef": {
                "hostId": "i-cca3d1c2"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "cr30jbwu9jstiasnykzizyh2a"
                  }
                ]
              }
            },
            {
              "name": "yarn-RESOURCEMANAGER-8691fd757828375a41864f9ab0ce2cd4",
              "type": "RESOURCEMANAGER",
              "hostRef": {
                "hostId": "i-03ff8d0d"
              },
              "config": {
                "items": [
                  {
                    "name": "rm_id",
                    "value": "53"
                  },
                  {
                    "name": "role_jceks_password",
                    "value": "eb4zwmjeudv5kesg7a3z10kfu"
                  }
                ]
              }
            }
          ],
          "displayName": "YARN (MR2 Included)"
        },
        {
          "name": "hdfs",
          "type": "HDFS",
          "config": {
            "roleTypeConfigs": [
              {
                "roleType": "BALANCER",
                "items": [
                  {
                    "name": "balancer_java_heapsize",
                    "value": "593494016"
                  }
                ]
              },
              {
                "roleType": "DATANODE",
                "items": [
                  {
                    "name": "dfs_data_dir_list",
                    "value": "/dfs/dn"
                  },
                  {
                    "name": "dfs_datanode_du_reserved",
                    "value": "10736126771"
                  }
                ]
              },
              {
                "roleType": "GATEWAY",
                "items": [
                  {
                    "name": "dfs_client_use_trash",
                    "value": "true"
                  }
                ]
              },
              {
                "roleType": "NAMENODE",
                "items": [
                  {
                    "name": "dfs_name_dir_list",
                    "value": "/dfs/nn"
                  },
                  {
                    "name": "dfs_namenode_servicerpc_address",
                    "value": "8022"
                  },
                  {
                    "name": "namenode_java_heapsize",
                    "value": "593494016"
                  }
                ]
              },
              {
                "roleType": "SECONDARYNAMENODE",
                "items": [
                  {
                    "name": "fs_checkpoint_dir_list",
                    "value": "/dfs/snn"
                  },
                  {
                    "name": "secondary_namenode_java_heapsize",
                    "value": "593494016"
                  }
                ]
              }
            ],
            "items": [
              {
                "name": "dfs_ha_fencing_cloudera_manager_secret_key",
                "value": "dsIanbeiBCnHAjGUAEjkF071HBroqP"
              },
              {
                "name": "fc_authorization_secret_key",
                "value": "garkVSrAAn3g1TyABi4YOBa8NyaU9H"
              },
              {
                "name": "http_auth_signature_secret",
                "value": "pv4sTc1THZ8S1aCQJNwLhYJsxWlRRA"
              },
              {
                "name": "rm_dirty",
                "value": "true"
              },
              {
                "name": "zookeeper_service",
                "value": "zookeeper"
              }
            ]
          },
          "roles": [
            {
              "name": "hdfs-BALANCER-8691fd757828375a41864f9ab0ce2cd4",
              "type": "BALANCER",
              "hostRef": {
                "hostId": "i-03ff8d0d"
              },
              "config": {
                "items": []
              }
            },
            {
              "name": "hdfs-DATANODE-6b9563b4ee2e8483d8b994c73f15e46a",
              "type": "DATANODE",
              "hostRef": {
                "hostId": "i-a3007dad"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "7yg1gf3v7qfnac1es3xcjwvbv"
                  }
                ]
              }
            },
            {
              "name": "hdfs-DATANODE-a8d991003cb9a7b756adf029e4c6d220",
              "type": "DATANODE",
              "hostRef": {
                "hostId": "i-a0007dae"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "7uyfjgek640p1y3oxj35xo80n"
                  }
                ]
              }
            },
            {
              "name": "hdfs-DATANODE-ae9f629b2be1b2161a198e7af1d74e66",
              "type": "DATANODE",
              "hostRef": {
                "hostId": "i-a1007daf"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "rajmpk8q1l93td6fjciplyca"
                  }
                ]
              }
            },
            {
              "name": "hdfs-DATANODE-d8c2c1bda620c2c5efe85ae4915ad489",
              "type": "DATANODE",
              "hostRef": {
                "hostId": "i-cca3d1c2"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "43u9eicp6q2ylfhobym7shzm7"
                  }
                ]
              }
            },
            {
              "name": "hdfs-NAMENODE-8691fd757828375a41864f9ab0ce2cd4",
              "type": "NAMENODE",
              "hostRef": {
                "hostId": "i-03ff8d0d"
              },
              "config": {
                "items": [
                  {
                    "name": "namenode_id",
                    "value": "55"
                  },
                  {
                    "name": "role_jceks_password",
                    "value": "9gm9advjokwno650s5t8bhecq"
                  }
                ]
              }
            },
            {
              "name": "hdfs-SECONDARYNAMENODE-8691fd757828375a41864f9ab0ce2cd4",
              "type": "SECONDARYNAMENODE",
              "hostRef": {
                "hostId": "i-03ff8d0d"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "eula7ndvh11hpxkf0gze0hy68"
                  }
                ]
              }
            }
          ],
          "displayName": "HDFS"
        }
      ]
    }
  ],
  "hosts": [
    {
      "hostId": "i-03ff8d0d",
      "ipAddress": "172.31.50.73",
      "hostname": "ip-172-31-50-73.ec2.internal",
      "rackId": "/default",
      "config": {
        "items": []
      }
    },
    {
      "hostId": "i-cca3d1c2",
      "ipAddress": "172.31.59.253",
      "hostname": "ip-172-31-59-253.ec2.internal",
      "rackId": "/default",
      "config": {
        "items": []
      }
    },
    {
      "hostId": "i-a3007dad",
      "ipAddress": "172.31.62.138",
      "hostname": "ip-172-31-62-138.ec2.internal",
      "rackId": "/default",
      "config": {
        "items": []
      }
    },
    {
      "hostId": "i-a0007dae",
      "ipAddress": "172.31.62.139",
      "hostname": "ip-172-31-62-139.ec2.internal",
      "rackId": "/default",
      "config": {
        "items": []
      }
    },
    {
      "hostId": "i-a1007daf",
      "ipAddress": "172.31.62.140",
      "hostname": "ip-172-31-62-140.ec2.internal",
      "rackId": "/default",
      "config": {
        "items": []
      }
    }
  ],
  "users": [
    {
      "name": "__cloudera_internal_user__mgmt-EVENTSERVER-8691fd757828375a41864f9ab0ce2cd4",
      "roles": [
        "ROLE_USER"
      ],
      "pwHash": "314cb5706f1c51892f2666dfc3fcbd0a873cde39ff194fec054efa2a5acef734",
      "pwSalt": 3054218850524064233,
      "pwLogin": true
    },
    {
      "name": "__cloudera_internal_user__mgmt-HOSTMONITOR-8691fd757828375a41864f9ab0ce2cd4",
      "roles": [
        "ROLE_USER"
      ],
      "pwHash": "7005690b16bf17d1a2f4e12e60f0f54354969a73e4138e0ebb1b39e4e626d6ba",
      "pwSalt": 3579342571845917143,
      "pwLogin": true
    },
    {
      "name": "__cloudera_internal_user__mgmt-REPORTSMANAGER-8691fd757828375a41864f9ab0ce2cd4",
      "roles": [
        "ROLE_USER"
      ],
      "pwHash": "c567c582edae66c24d1180b958db961acb6e05b662e0d9302f175da7d21e80fd",
      "pwSalt": -21720764349468236,
      "pwLogin": true
    },
    {
      "name": "__cloudera_internal_user__mgmt-SERVICEMONITOR-8691fd757828375a41864f9ab0ce2cd4",
      "roles": [
        "ROLE_USER"
      ],
      "pwHash": "72fa3428f7c418c177397da4b68a1e73c902cf732d2956bd29fc44701e093c7f",
      "pwSalt": -4081165415679463881,
      "pwLogin": true
    },
    {
      "name": "admin",
      "roles": [
        "ROLE_ADMIN"
      ],
      "pwHash": "9790fe68807d8145be48c910b9524130db306cad61de15ede4a546e2f5c52b50",
      "pwSalt": -4340461265399023081,
      "pwLogin": true
    },
    {
      "name": "minotaur",
      "roles": [
        "ROLE_CONFIGURATOR"
      ],
      "pwHash": "d821acb630e4c6598d1cf9c7964fd2a6c1fdaf110225d554aca950f3a899caaa",
      "pwSalt": -3645724454059255292,
      "pwLogin": true
    }
  ],
  "versionInfo": {
    "version": "5.8.2",
    "buildUser": "jenkins",
    "buildTimestamp": "20160916-1419",
    "gitHash": "d23c620f3a3bbd85d8511d6ebba49beaaab14b75",
    "snapshot": false
  },
  "managementService": {
    "name": "mgmt",
    "type": "MGMT",
    "config": {
      "roleTypeConfigs": [
        {
          "roleType": "EVENTSERVER",
          "items": [
            {
              "name": "event_server_heapsize",
              "value": "593494016"
            }
          ]
        },
        {
          "roleType": "HOSTMONITOR",
          "items": [
            {
              "name": "firehose_heapsize",
              "value": "593494016"
            },
            {
              "name": "firehose_non_java_memory_bytes",
              "value": "805306368"
            }
          ]
        },
        {
          "roleType": "REPORTSMANAGER",
          "items": [
            {
              "name": "headlamp_database_host",
              "value": "ip-172-31-50-73.ec2.internal"
            },
            {
              "name": "headlamp_database_name",
              "value": "reports"
            },
            {
              "name": "headlamp_database_password",
              "value": "password"
            },
            {
              "name": "headlamp_database_user",
              "value": "reports"
            },
            {
              "name": "headlamp_heapsize",
              "value": "593494016"
            }
          ]
        },
        {
          "roleType": "SERVICEMONITOR",
          "items": [
            {
              "name": "firehose_heapsize",
              "value": "593494016"
            },
            {
              "name": "firehose_non_java_memory_bytes",
              "value": "805306368"
            }
          ]
        }
      ],
      "items": []
    },
    "roles": [
      {
        "name": "mgmt-ALERTPUBLISHER-8691fd757828375a41864f9ab0ce2cd4",
        "type": "ALERTPUBLISHER",
        "hostRef": {
          "hostId": "i-03ff8d0d"
        },
        "config": {
          "items": [
            {
              "name": "role_jceks_password",
              "value": "dvfwt02dl26ws6uzt7r1nhx9w"
            }
          ]
        }
      },
      {
        "name": "mgmt-EVENTSERVER-8691fd757828375a41864f9ab0ce2cd4",
        "type": "EVENTSERVER",
        "hostRef": {
          "hostId": "i-03ff8d0d"
        },
        "config": {
          "items": [
            {
              "name": "role_jceks_password",
              "value": "6p9qdzy2stu91je3g52srieq6"
            }
          ]
        }
      },
      {
        "name": "mgmt-HOSTMONITOR-8691fd757828375a41864f9ab0ce2cd4",
        "type": "HOSTMONITOR",
        "hostRef": {
          "hostId": "i-03ff8d0d"
        },
        "config": {
          "items": [
            {
              "name": "role_jceks_password",
              "value": "9hwd0slh8dxv4rule4mw29g6w"
            }
          ]
        }
      },
      {
        "name": "mgmt-REPORTSMANAGER-8691fd757828375a41864f9ab0ce2cd4",
        "type": "REPORTSMANAGER",
        "hostRef": {
          "hostId": "i-03ff8d0d"
        },
        "config": {
          "items": [
            {
              "name": "role_jceks_password",
              "value": "d171yr8z30k0vrnegb8ma6ruk"
            }
          ]
        }
      },
      {
        "name": "mgmt-SERVICEMONITOR-8691fd757828375a41864f9ab0ce2cd4",
        "type": "SERVICEMONITOR",
        "hostRef": {
          "hostId": "i-03ff8d0d"
        },
        "config": {
          "items": [
            {
              "name": "role_jceks_password",
              "value": "4lt3aml51ch9yp38e3upbvw3e"
            }
          ]
        }
      }
    ],
    "displayName": "Cloudera Management Service"
  },
  "managerSettings": {
    "items": [
      {
        "name": "CLUSTER_STATS_START",
        "value": "10/21/2012 2:30"
      },
      {
        "name": "PUBLIC_CLOUD_STATUS",
        "value": "ON_PUBLIC_CLOUD"
      },
      {
        "name": "REMOTE_PARCEL_REPO_URLS",
        "value": "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
      }
    ]
  }
}
```