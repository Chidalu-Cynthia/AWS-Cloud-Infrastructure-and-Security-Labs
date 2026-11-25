# AWS VPC Networking Lab

## 1. Project Overview and Objectives

Designed and configured a custom AWS Virtual Private Cloud (VPC) across two Availability Zones. The project focused on network segmentation, subnet design, internet connectivity, routing, and network access control.

## 2. Architecture and Resource Design

Created a VPC with the IPv4 CIDR block `10.0.0.0/16`, divided into four subnets across two Availability Zones:

| Subnet | CIDR Block | Type |
|---|---|---|
| Public Subnet AZ1 | `10.0.1.0/24` | Public |
| Private Subnet AZ1 | `10.0.2.0/24` | Private |
| Public Subnet AZ2 | `10.0.3.0/24` | Public |
| Private Subnet AZ2 | `10.0.4.0/24` | Private |

## 3. AWS Services and Configurations

- **Amazon VPC:** Created the custom VPC.
- **Subnets:** Created four subnets across two Availability Zones.
- **Internet Gateway:** Created and attached `CloudSecurity-IGW`.
- **Route Tables:** Created separate public and private route tables.
- **Security Group:** Configured inbound access rules to control network traffic.

## 4. Implementation and Key Decisions

- Configured the public route table with the local VPC route and a default route (`0.0.0.0/0`) through the Internet Gateway.
- Kept the private route table limited to local VPC routing, without a direct Internet Gateway route.
- Associated the route tables with their intended subnets.
- Used separate public and private subnets to establish network segmentation across both Availability Zones.

## 5. Security Considerations

- Separated public-facing and private network resources.
- Restricted inbound access through security group rules.
- Avoided exposing private subnets through a direct Internet Gateway route.
- Used network segmentation to control how resources communicate.

## 6. Testing and Validation

- Reviewed the VPC and four subnet configurations.
- Confirmed that the Internet Gateway was attached to the VPC.
- Reviewed public and private route table configurations and subnet associations.
- Inspected the security group's inbound rules.

## 7. Troubleshooting and Findings

The project reinforced an important networking principle: a subnet is not public simply because of its name. Its route table determines whether it has a route to an Internet Gateway. Private subnets without that route do not have direct internet access through the Internet Gateway.

## 8. Lessons Learned

- How IPv4 CIDR blocks are used to plan and divide VPC networks.
- How Availability Zones support network distribution.
- How route tables determine traffic paths.
- The difference between public and private subnet routing.
- How security groups control inbound and outbound traffic at the resource level.

## Evidence

- [View Internet Gateway Attachment](screenshots/Creatd%20and%20attached%20internet%20gateway.png)
- [View Four Created Subnets](screenshots/Created%20four%20subnets.png)
- [View Security Group Inbound Rules](screenshots/created%20inbound%20rules%20for%20my%20security%20Group.png)
- [View Route Table](screenshots/created%20route%20table.png)
