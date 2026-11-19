# AWS EFS Storage Lab

## Overview
Configured Amazon Elastic File System (EFS) and mounted shared storage on an Ubuntu EC2 instance.

## Configurations & Activities
- Created an encrypted EFS file system.
![Encrypted EFS File System Created](screenshots/Created%20an%20encrypted%20EFS%20file%20system.png)
- Configured mount targets across two Availability Zones.
- Configured security groups for NFS traffic (TCP 2049).
![EFS NFS Security Group Inbound Rule](screenshots/NFS%20security-group%20inbound%20rule%20(TCP%202049)..png)
- Mounted the file system on the Ubuntu EC2 instance.
![Successful EFS Mount on Ubuntu](screenshots/Successful%20EFS%20mount%20on%20Ubuntu..png)
- Troubleshot a connection timeout caused by a missing EC2 security group source in the EFS inbound rule.
- Created a test file and verified data persistence after unmounting and remounting EFS.
![EFS Data Persistence Verified](screenshots/Created%20a%20test%20file%20and%20verified%20data%20persistence%20after%20unmounting%20and%20remounting%20EFS.png)

## Key Skills
EFS configuration · NFS · Security groups · Linux mounting · Shared storage · Troubleshooting
