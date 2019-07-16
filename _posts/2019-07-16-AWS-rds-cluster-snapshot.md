---
title: "AWS Cli - RDS Cluster Snapshot"
image: 
  path:  /images/AWS-rds-snapshot-cli.png
  thumbnail: /images/AWS-rds-snapshot-cli.png

categories:
  - AWS 
tags:
  - AWS
  - RDS
  - SNAPSHOT
  - AWS-CLI 
--- 

# AWS Cli Series - Example for RDS Cluster Snapshot 


~~~shell 

$ aws rds create-db-cluster-snapshot --db-cluster-snapshot-identifier test-rds-cluster-final-snapshot-1507-2019 \
--db-cluster-identifier test-rds-cluster --tags Key=Name,Value=test-rds-cluster-final-snapshot-1507-2019 
---------------------------------------------------------------------------------------------------------------------------------------------
|                                                          CreateDBClusterSnapshot                                                          |
+-------------------------------------------------------------------------------------------------------------------------------------------+
||                                                            DBClusterSnapshot                                                            ||
|+-----------------------------------+-----------------------------------------------------------------------------------------------------+|
||  AllocatedStorage                 |  1                                                                                                  ||
||  ClusterCreateTime                |  2019-03-10T19:53:50.658Z                                                                           ||
||  DBClusterIdentifier              |  test-rds-cluster                                                                                   ||
||  DBClusterSnapshotArn             |  arn:aws:rds:eu-west-1:XXXXXXX:cluster-snapshot:test-rds-cluster-final-snapshot-1507-2019           ||
||  DBClusterSnapshotIdentifier      |  test-rds-cluster-final-snapshot-1507-2019                                                          ||
||  Engine                           |  aurora                                                                                             ||
||  EngineVersion                    |  5.6.10a                                                                                            ||
||  IAMDatabaseAuthenticationEnabled |  True                                                                                               ||
||  KmsKeyId                         |  arn:aws:kms:eu-west-1:XXXXX6:key/XXXXXXXXXXX 							   ||
||  LicenseModel                     |  aurora                                                                                             ||
||  MasterUsername                   |  dbadmin                                                                                            ||
||  PercentProgress                  |  0                                                                                                  ||
||  Port                             |  0                                                                                                  ||
||  SnapshotCreateTime               |  2019-07-15T06:19:20.733Z                                                                           ||
||  SnapshotType                     |  manual                                                                                             ||
||  Status                           |  creating                                                                                           ||
||  StorageEncrypted                 |  True                                                                                               ||
||  VpcId                            |  vpc-XXXXXXXX 		                                                                           ||
|+-----------------------------------+-----------------------------------------------------------------------------------------------------+|
|||                                                           AvailabilityZones                                                           |||
||+---------------------------------------------------------------------------------------------------------------------------------------+||
|||  eu-west-1a                                                                                                                           |||
|||  eu-west-1b                                                                                                                           |||
|||  eu-west-1c                                                                                                                           |||
||+---------------------------------------------------------------------------------------------------------------------------------------+||


$ aws rds describe-db-cluster-snapshots --db-cluster-identifier  test-rds-cluster 

||+---------------------------------------------------------------------------------------------------------------------------------------+||
||                                                           DBClusterSnapshots                                                            ||
|+-----------------------------------+-----------------------------------------------------------------------------------------------------+|
||  AllocatedStorage                 |  59                                                                                                 ||
||  ClusterCreateTime                |  2019-03-10T19:53:50.658Z                                                                           ||
||  DBClusterIdentifier              |  test-rds-cluster                                                                                   ||
||  DBClusterSnapshotArn             |  arn:aws:rds:eu-west-1:XXXXXXXXXXXX:cluster-snapshot:test-rds-cluster-final-snapshot-1507-2019      ||
||  DBClusterSnapshotIdentifier      |  test-rds-cluster-final-snapshot-1507-2019                                                          ||
||  Engine                           |  aurora                                                                                             ||
||  EngineVersion                    |  5.6.10a                                                                                            ||
||  IAMDatabaseAuthenticationEnabled |  True                                                                                               ||
||  KmsKeyId                         |  arn:aws:kms:eu-west-XXXXXXXX:key/XXXXXXXXXXXXX                       				   ||
||  LicenseModel                     |  aurora                                                                                             ||
||  MasterUsername                   |  dbadmin                                                                                            ||
||  PercentProgress                  |  100                                                                                                ||
||  Port                             |  0                                                                                                  ||
||  SnapshotCreateTime               |  2019-07-15T06:19:20.733Z                                                                           ||
||  SnapshotType                     |  manual                                                                                             ||
||  Status                           |  available                                                                                          ||
||  StorageEncrypted                 |  True                                                                                               ||
||  VpcId                            |  vpc-XXXXXXXXXXXXXXXXX                                                                              ||
|+-----------------------------------+-----------------------------------------------------------------------------------------------------+|
|||                                                           AvailabilityZones                                                           |||
||+---------------------------------------------------------------------------------------------------------------------------------------+||
|||  eu-west-1a                                                                                                                           |||
|||  eu-west-1b                                                                                                                           |||
|||  eu-west-1c                                                                                                                           |||
||+---------------------------------------------------------------------------------------------------------------------------------------+||

~~~ 



