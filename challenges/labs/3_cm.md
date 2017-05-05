*The command and output for hdfs dfs -ls /user

		[hdfs@mycloudera1 ~]$ hdfs dfs -ls /user
		Found 9 items
		drwxr-xr-x   - admin  admin               0 2017-05-05 04:18 /user/admin
		drwxr-xr-x   - hdfs   supergroup          0 2017-05-05 04:19 /user/cate
		drwxr-xr-x   - hdfs   supergroup          0 2017-05-05 04:18 /user/hdfs
		drwxrwxrwx   - mapred hadoop              0 2017-05-05 04:06 /user/history
		drwxrwxr-t   - hive   hive                0 2017-05-05 04:06 /user/hive
		drwxrwxr-x   - hue    hue                 0 2017-05-05 04:07 /user/hue
		drwxrwxr-x   - impala impala              0 2017-05-05 04:07 /user/impala
		drwxr-xr-x   - hdfs   supergroup          0 2017-05-05 04:19 /user/jemaine
		drwxrwxr-x   - oozie  oozie               0 2017-05-05 04:08 /user/oozie
		[hdfs@mycloudera1 ~]$

*User Directory
<center> <img src="https://github.com/jimmyrekso/SEBC/blob/master/challenges/labs/images/hdfs_folder.png"/> </center>



*The command and output from the CM API call ../api/v14/hosts
		{
		"items" : [ {
			"hostId" : "b2ab651e-bac8-4d60-a01c-831809916476",
			"ipAddress" : "10.146.0.6",
			"hostname" : "mycloudera1.jimmy",
			"rackId" : "/default",
			"hostUrl" : "http://mycloudera1.jimmy:7180/cmf/hostRedirect/b2ab651e-bac8-4d60-a01c-831809916476",
			"maintenanceMode" : false,
			"maintenanceOwners" : [ ],
			"commissionState" : "COMMISSIONED",
			"numCores" : 2,
			"numPhysicalCores" : 1,
			"totalPhysMemBytes" : 10485829632
		}, {
			"hostId" : "81faba90-17c7-4786-940b-3b60fe207f7e",
			"ipAddress" : "10.146.0.5",
			"hostname" : "mycloudera2.jimmy",
			"rackId" : "/default",
			"hostUrl" : "http://mycloudera1.jimmy:7180/cmf/hostRedirect/81faba90-17c7-4786-940b-3b60fe207f7e",
			"maintenanceMode" : false,
			"maintenanceOwners" : [ ],
			"commissionState" : "COMMISSIONED",
			"numCores" : 2,
			"numPhysicalCores" : 1,
			"totalPhysMemBytes" : 10485829632
		}, {
			"hostId" : "6c7548de-73ec-4bd1-aa0a-ded66b5da78f",
			"ipAddress" : "10.146.0.7",
			"hostname" : "mycloudera3.jimmy",
			"rackId" : "/default",
			"hostUrl" : "http://mycloudera1.jimmy:7180/cmf/hostRedirect/6c7548de-73ec-4bd1-aa0a-ded66b5da78f",
			"maintenanceMode" : false,
			"maintenanceOwners" : [ ],
			"commissionState" : "COMMISSIONED",
			"numCores" : 2,
			"numPhysicalCores" : 1,
			"totalPhysMemBytes" : 10485829632
		}, {
			"hostId" : "19db5501-1d71-44f8-89a8-4052f281c6ea",
			"ipAddress" : "10.146.0.8",
			"hostname" : "mycloudera4.jimmy",
			"rackId" : "/default",
			"hostUrl" : "http://mycloudera1.jimmy:7180/cmf/hostRedirect/19db5501-1d71-44f8-89a8-4052f281c6ea",
			"maintenanceMode" : false,
			"maintenanceOwners" : [ ],
			"commissionState" : "COMMISSIONED",
			"numCores" : 2,
			"numPhysicalCores" : 1,
			"totalPhysMemBytes" : 10485829632
		} ]
		}

<center> <img src="https://github.com/jimmyrekso/SEBC/blob/master/challenges/labs/images/api_host.png"/> </center>

*The command and output from the CM API call ../api/v6/clusters/<githubName>/services
		{
		"items" : [ {
			"name" : "hive",
			"type" : "HIVE",
			"clusterRef" : {
			"clusterName" : "cluster"
			},
			"serviceUrl" : "http://mycloudera1.jimmy:7180/cmf/serviceRedirect/hive",
			"serviceState" : "STARTED",
			"healthSummary" : "GOOD",
			"healthChecks" : [ {
			"name" : "HIVE_HIVEMETASTORES_HEALTHY",
			"summary" : "GOOD"
			}, {
			"name" : "HIVE_HIVESERVER2S_HEALTHY",
			"summary" : "GOOD"
			}, {
			"name" : "HIVE_WEBHCATS_HEALTHY",
			"summary" : "GOOD"
			} ],
			"configStalenessStatus" : "FRESH",
			"clientConfigStalenessStatus" : "FRESH",
			"maintenanceMode" : false,
			"maintenanceOwners" : [ ],
			"displayName" : "Hive"
		}, {
			"name" : "zookeeper",
			"type" : "ZOOKEEPER",
			"clusterRef" : {
			"clusterName" : "cluster"
			},
			"serviceUrl" : "http://mycloudera1.jimmy:7180/cmf/serviceRedirect/zookeeper",
			"serviceState" : "STARTED",
			"healthSummary" : "GOOD",
			"healthChecks" : [ {
			"name" : "ZOOKEEPER_CANARY_HEALTH",
			"summary" : "GOOD"
			}, {
			"name" : "ZOOKEEPER_SERVERS_HEALTHY",
			"summary" : "GOOD"
			} ],
			"configStalenessStatus" : "FRESH",
			"clientConfigStalenessStatus" : "FRESH",
			"maintenanceMode" : false,
			"maintenanceOwners" : [ ],
			"displayName" : "ZooKeeper"
		}, {
			"name" : "hue",
			"type" : "HUE",
			"clusterRef" : {
			"clusterName" : "cluster"
			},
			"serviceUrl" : "http://mycloudera1.jimmy:7180/cmf/serviceRedirect/hue",
			"serviceState" : "STARTED",
			"healthSummary" : "GOOD",
			"healthChecks" : [ {
			"name" : "HUE_HUE_SERVERS_HEALTHY",
			"summary" : "GOOD"
			} ],
			"configStalenessStatus" : "FRESH",
			"clientConfigStalenessStatus" : "FRESH",
			"maintenanceMode" : false,
			"maintenanceOwners" : [ ],
			"displayName" : "Hue"
		}, {
			"name" : "oozie",
			"type" : "OOZIE",
			"clusterRef" : {
			"clusterName" : "cluster"
			},
			"serviceUrl" : "http://mycloudera1.jimmy:7180/cmf/serviceRedirect/oozie",
			"serviceState" : "STARTED",
			"healthSummary" : "GOOD",
			"healthChecks" : [ {
			"name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
			"summary" : "GOOD"
			} ],
			"configStalenessStatus" : "FRESH",
			"clientConfigStalenessStatus" : "FRESH",
			"maintenanceMode" : false,
			"maintenanceOwners" : [ ],
			"displayName" : "Oozie"
		}, {
			"name" : "impala",
			"type" : "IMPALA",
			"clusterRef" : {
			"clusterName" : "cluster"
			},
			"serviceUrl" : "http://mycloudera1.jimmy:7180/cmf/serviceRedirect/impala",
			"serviceState" : "STARTED",
			"healthSummary" : "GOOD",
			"healthChecks" : [ {
			"name" : "IMPALA_ASSIGNMENT_LOCALITY",
			"summary" : "DISABLED"
			}, {
			"name" : "IMPALA_CATALOGSERVER_HEALTH",
			"summary" : "GOOD"
			}, {
			"name" : "IMPALA_IMPALADS_HEALTHY",
			"summary" : "GOOD"
			}, {
			"name" : "IMPALA_STATESTORE_HEALTH",
			"summary" : "GOOD"
			} ],
			"configStalenessStatus" : "FRESH",
			"clientConfigStalenessStatus" : "FRESH",
			"maintenanceMode" : false,
			"maintenanceOwners" : [ ],
			"displayName" : "Impala"
		}, {
			"name" : "yarn",
			"type" : "YARN",
			"clusterRef" : {
			"clusterName" : "cluster"
			},
			"serviceUrl" : "http://mycloudera1.jimmy:7180/cmf/serviceRedirect/yarn",
			"serviceState" : "STARTED",
			"healthSummary" : "GOOD",
			"healthChecks" : [ {
			"name" : "YARN_JOBHISTORY_HEALTH",
			"summary" : "GOOD"
			}, {
			"name" : "YARN_NODE_MANAGERS_HEALTHY",
			"summary" : "GOOD"
			}, {
			"name" : "YARN_RESOURCEMANAGERS_HEALTH",
			"summary" : "GOOD"
			}, {
			"name" : "YARN_USAGE_AGGREGATION_HEALTH",
			"summary" : "DISABLED"
			} ],
			"configStalenessStatus" : "FRESH",
			"clientConfigStalenessStatus" : "FRESH",
			"maintenanceMode" : false,
			"maintenanceOwners" : [ ],
			"displayName" : "YARN (MR2 Included)"
		}, {
			"name" : "hdfs",
			"type" : "HDFS",
			"clusterRef" : {
			"clusterName" : "cluster"
			},
			"serviceUrl" : "http://mycloudera1.jimmy:7180/cmf/serviceRedirect/hdfs",
			"serviceState" : "STARTED",
			"healthSummary" : "GOOD",
			"healthChecks" : [ {
			"name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
			"summary" : "GOOD"
			}, {
			"name" : "HDFS_CANARY_HEALTH",
			"summary" : "GOOD"
			}, {
			"name" : "HDFS_DATA_NODES_HEALTHY",
			"summary" : "GOOD"
			}, {
			"name" : "HDFS_FREE_SPACE_REMAINING",
			"summary" : "GOOD"
			}, {
			"name" : "HDFS_HA_NAMENODE_HEALTH",
			"summary" : "GOOD"
			}, {
			"name" : "HDFS_MISSING_BLOCKS",
			"summary" : "GOOD"
			}, {
			"name" : "HDFS_UNDER_REPLICATED_BLOCKS",
			"summary" : "GOOD"
			} ],
			"configStalenessStatus" : "FRESH",
			"clientConfigStalenessStatus" : "FRESH",
			"maintenanceMode" : false,
			"maintenanceOwners" : [ ],
			"displayName" : "HDFS"
		} ]
		}
<center> <img src="https://github.com/jimmyrekso/SEBC/blob/master/challenges/labs/images/api_cluster.png"/> </center>		



*Capture a Hue screen that shows the Hive tables to challenges/labs/3_hue_hive.png
<center> <img src="https://github.com/jimmyrekso/SEBC/blob/master/challenges/labs/hue_hive.png"/> </center>		
