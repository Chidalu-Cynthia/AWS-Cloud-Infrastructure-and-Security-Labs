# AWS EC2 & Linux Lab

## Overview
Launched and configured an Ubuntu EC2 instance within the custom VPC.


### Ubuntu EC2 Instance Launched

![Launched Ubuntu EC2 Instance](screenshots/Launched%20Ubuntu%20EC2%20Instance.png)
- ## EC2 Instance Configuration
- **AMI:** Ubuntu Server 26.04 LTS.
- **Instance Type:** `t3.micro`.
- **Network:** Deployed in a public subnet with a public IP.
- **Security Group:** SSH access (TCP 22) restricted to my IP address.
- **Storage:** 8 GiB encrypted EBS root volume.
- **Instance Security:** IMDSv2 enforced; CPU credit mode set to Standard.
- **Access:** Connected securely using SSH key authentication.

![EC2 Instance Configuration](screenshots/Instance%20Configuration.jpeg)
### Successful SSH Connection

![Successful SSH Connection](screenshots/Successful%20SSH%20Connection.png)

## Linux Practice
- Updated and maintained the Ubuntu system.
- Practised Linux commands, file management, and permissions.
- Explored users, groups, and privilege management.

## Key Skills
EC2 deployment · SSH · Linux administration · EBS encryption · Instance security
