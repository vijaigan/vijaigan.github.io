---
title: "AWS: ec2 instance cloning cross region "
categories:
  - AWS
tags:
  - ec2
  - AMI
last_modified_at: 2019-03-28
--- 
Many times, we might need to copy AMI images for cloning ec2 instances cross region on AWS. 
This script provided basic funtionality for creating AMI image for a given instanceid and copies the AMI Image to the Destionation Region.  The script will take wait till the AMI image is fully created and available and copies the same to Destination Region. 

https://github.com/vijaigan/AWS/blob/master/ec2-clone/ec2-clone-region.sh 


#### Variables need to updated 
Update the DST_REGION,SRC_REGION and INSTANCE_ID . that's it. 


Example output 
~~~~
Working on XXX-T1 
ami-0fcc23axxxx is created for XXX-T1 
Waiting for create-ami for ami-0fcc23ad9xxxx to finish
........................
ami-0be5decaxxx created in eu-west-1 with Name XXX-AMI-2019-03-27 from source ami-0fcc23adxxxxx from ap-southeast-1
~~~~