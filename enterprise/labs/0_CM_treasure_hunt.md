# What is ubertask optimization?

Runs "sufficiently small" jobs sequentially within a single JVM

# Where in CM is the Kerberos Security Realm value displayed?

config: Kerberos Security Realm

# Which CDH service(s) host a property for enabling Kerberos authentication?

HDFS Service (Datanodes config DataNode HTTP Web UI Port and DataNode Transceiver Port)

# How do you upgrade the CM agents?

Manually or using Cloudera Upgrade Manager

# Give the tsquery statement used to chart Hue's CPU utilization?

Select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=$SERVICENAME

# Name all the roles that make up the Hive service

Hive Metastore Server, HiverServer2, Hosts

# What steps must be completed before integrating Cloudera Manager with Kerberos?
	* Setup a working MIT KDC or Active Directory that allows renewable tickets with non-zero ticket lifetimes on KDC server (Can be CM)
	* Install (kerberos Client) to all nodes
	* Create an account for Cloudera Manager that has the permissions to create other accounts in the KDC
	* KDC Information
	* KRB5 Configuration
	* Configure HDFS DataNode Ports