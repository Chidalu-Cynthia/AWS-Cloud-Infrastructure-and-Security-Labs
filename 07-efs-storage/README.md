# AWS EFS Storage Lab

## Overview
Configured Amazon Elastic File System (EFS) and mounted shared storage on an Ubuntu EC2 instance.

## Configurations & Activities
- Created an encrypted EFS file system.
![Encrypted EFS File System Created](screenshots/Created%20an%20encrypted%20EFS%20file%20system.png)
- Configured mount targets across two Availability Zones.
- Configured security groups for NFS traffic (TCP 2049).
- Mounted the file system on the Ubuntu EC2 instance.
![Successful EFS Mount on Ubuntu](screenshots/Successful%20EFS%20mount%20on%20Ubuntu..png)
- Troubleshot a connection timeout caused by a missing EC2 security group source in the EFS inbound rule.
- Created a test file and verified data persistence after unmounting and remounting EFS.

## Key Skills
EFS configuration · NFS · Security groups · Linux mounting · Shared storage · Troubleshooting
