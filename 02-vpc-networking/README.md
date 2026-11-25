# AWS VPC Networking Lab

## Overview
Designed and configured a custom AWS network across two Availability Zones.

## Configurations
- **VPC:** `10.0.0.0/16`
- **Subnets:** Four (two public and two private).
- **Internet Gateway:** `CloudSecurity-IGW`, attached to the VPC.
- **Route Tables:** Separate public and private route tables.
- **Routing:** Public default route (`0.0.0.0/0`) through the Internet Gateway.
- **Security Group:** Configured inbound access controls.

## Key Skills
VPC design · Subnetting · Route tables · Internet connectivity · Network segmentation · Security groups
## Evidence

### Internet Gateway Attached to VPC

![Internet Gateway Attached](screenshots/Creatd%20and%20attached%20internet%20gateway.png)

- [View Four Created Subnets](screenshots/Created%20four%20subnets.png)
- [View Security Group Inbound Rules](screenshots/created%20inbound%20rules%20for%20my%20security%20Group.png)
- [View Route Table](screenshots/created%20route%20table.png)
