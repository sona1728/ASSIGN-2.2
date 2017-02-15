*HADOOP 1.x COMPONENTS:

Hadoop 1.x Major Components components are: HDFS and MapReduce. They are also know as “Two Pillars” of Hadoop 1.x.

HDFS:
HDFS is a Hadoop Distributed FileSystem, where our BigData is stored using Commodity Hardware. It is designed to work with Large DataSets with default block size is 64MB (We can change it as per our Project requirements).

HDFS component is again divided into two sub-components:
NameNode:
• Contains the Hadoop FileSystem Tree and other metadata information about files and directories.
• Contains in-memory mapping of which blocks are stored in which datanode.
Secondary NameNode
• Performs house-keeping activities for NameNodes, like the periodic merging of namespace and edits.
• This is not a back up for a NameNode.

DataNode:
• Stores actual data blocks of files in HDFS on its own local disk.
• Sends signals to the NameNode periodically (called as Heartbeat) to verify whether it is active.
• Sends block reporting to the NameNode on the cluster startup as well as periodically at every 10th Heartbeat.
• The DataNodes are the workhorses of a system.
• They perform all the block operations including periodic checksum. They receive instructions from the name node of
where to put the blocks and how to put them. 

MapReduce:
MapReduce is a Distributed Data Processing or Batch Processing Programming Model. Like HDFS, MapReduce component also uses Commodity Hardware to process “High Volume of Variety of Data at High Velocity Rate” in a reliable and fault-tolerant manner.

MapReduce component is again divided into two sub-components:

JobTracker (Not present in Hadoop 2.x):
• Controls the overall execution of the MapReduce jobs.

TaskTracker (Not present in Hadoop 2.x):
• Runs individual MapReduce jobs on DataNodes.
• Periodically communicates with the JobTracker to give updates and receive instructions.
