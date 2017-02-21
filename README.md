# 3.3


Q.List the components of Hadoop 2.x and explain them in detail.


-Hadoop Common Module is a Hadoop Base API (A Jar file) for all Hadoop Components. All other components works on top of this module.
-HDFS stands for Hadoop Distributed File System. It is also know as HDFS V2 as it is part of Hadoop 2.x with some enhanced features. It is used as a Distributed Storage System in Hadoop Architecture.
-YARN stands for Yet Another Resource Negotiator. It is new Component in Hadoop 2.x Architecture. It is also know as “MR V2”.
-MapReduce is a Batch Processing or Distributed Data Processing Module. It is also know as “MR V1” as it is part of Hadoop 1.x with some updated features.
-Remaining all Hadoop Ecosystem components work on top of these three major components: HDFS, YARN and MapReduce.

When compared to Hadoop 1.x, Hadoop 2.x Architecture is designed completely different. It has added one new component : YARN and also updated HDFS and MapReduce component’s Responsibilities.

Hadoop 2.x has the following three Major Components:

1.HDFS

2.YARN

3.MapReduce

These three are also known as Three Pillars of Hadoop 2. Here major key component change is YARN. It is really game changing component in BigData Hadoop System.

1.HDFS 2.x Daemons

The working methodology of HDFS 2.x daemons is same as it was in Hadoop 1.x Architecture with following differences.

Hadoop 2.x allows Multiple Name Nodes for HDFS Federation
New Architecture allows HDFS High Availability mode in which it can have Active and StandBy Name Nodes (No Need of Secondary Name Node in this case)
Hadoop 2.x Non HA mode has same Name Node and Secondary Name Node working same as in Hadoop 1.x architecture

2.MapReduce 2.x Daemons (YARN)

MapReduce2 has replace old daemon process Job Tracker and Task Tracker with YARN components Resource Manager and Node Manager respectively. These two components are responsible for executing distributed data computation jobs in Hadoop 2(Refer my post on YARN Architecture for further understanding).

Resource Manager

This daemon process runs on master node (may run on the same machine as name node for smaller clusters)
It is responsible for getting job submitted from client and schedule it on cluster, monitoring running jobs on cluster and allocating proper resources on the slave node
It communicates with Node Manager daemon process on the slave node to track the resource utilization
It uses two other processes named Application Manager and Scheduler for MapReduce task and resource management
Node Manager

This daemon process runs on slave nodes (normally on HDFS Data node machines)
It is responsible for coordinating with Resource Manager for task scheduling and tracking the resource utilization on the slave node
It also reports the resource utilization back to the Resource Manager
It uses other daemon process like Application Master and Container for MapReduce task scheduling and execution on the slave node

