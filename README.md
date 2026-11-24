
# AWS Cloud Infrastructure & Security Labs

A technical portfolio documenting practical work in AWS cloud infrastructure, networking, compute, storage, identity and access management, and cloud security.

This repository brings together hands-on deployments, configuration exercises, security testing, troubleshooting, and technical research. Each project documents the architecture, implementation decisions, security controls, validation results, and lessons learned.

The focus is not only on deploying AWS resources, but also on understanding how they communicate, how access is controlled, and how security is applied across a cloud environment.

## Project Objectives

- Design and understand AWS cloud infrastructure.
- Build network architectures using VPCs, subnets, route tables, and gateways.
- Deploy and administer compute resources.
- Configure cloud storage and encryption.
- Apply IAM roles and policies using least-privilege principles.
- Implement network and workload security controls.
- Explore monitoring, logging, and auditing.
- Validate configurations through CLI commands and practical tests.
- Document technical decisions, troubleshooting, and security findings.

## Project Index

| No. | Project | AWS Services / Technologies | Work Status |
|---|---|---|---|
| 01 | AWS Account Setup & Security | AWS Account, Root MFA, IAM | Hands-on |
| 02 | VPC Networking & Network Security | VPC, Subnets, Route Tables, Internet Gateway, Security Groups | Hands-on |
| 03 | EC2 Deployment & Linux Administration | EC2, Ubuntu, SSH, Nginx | Hands-on |
| 04 | Elastic Block Storage | EBS, Snapshots, KMS | Hands-on |
| 05 | Cloud Monitoring & Auditing | CloudWatch, CloudTrail | Hands-on exploration |
| 06 | Amazon S3 Storage & Security | S3, Bucket Policies, Versioning, Encryption | Hands-on |
| 07 | Elastic File System | EFS, NFS, Security Groups | Troubleshooting |
| 08 | IAM & Role-Based Access Control | IAM Roles, Policies, STS, AWS CLI | Hands-on |
| 09 | Application Load Balancing | ALB, EC2, Target Groups, Health Checks | Hands-on |
| 10 | Serverless Computing | AWS Lambda, IAM, CloudWatch Logs | Hands-on |
| 11 | Database Services & Security | RDS, Aurora, DynamoDB, KMS | Conceptual study and limited deployment |
| 12 | Content Delivery, DNS & Web Application Security | CloudFront, Route 53, AWS WAF | Conceptual study |

> **Work status matters:** Hands-on means I configured and tested the relevant resources. Troubleshooting means I investigated and documented an issue without claiming an unverified successful outcome. Conceptual study means I explored the architecture, features, and security controls without claiming a completed deployment.

## Technical Coverage

| Technical Area | Services / Technologies | Concepts and Skills |
|---|---|---|
| Cloud Networking | VPC, Subnets, Route Tables, Internet Gateway | CIDR planning, network segmentation, routing, public and private subnet design |
| Compute | EC2, Lambda | Instance deployment, Linux administration, serverless execution |
| Storage | S3, EBS, EFS | Object, block and shared file storage |
| Identity & Access Management | IAM, STS, AWS CLI | Roles, trust policies, permissions policies, temporary credentials, least privilege |
| Network Security | Security Groups, ALB | Traffic filtering, access restrictions, health checks, availability |
| Encryption | AWS KMS, EBS Encryption, S3 Encryption | Encryption at rest and key management concepts |
| Monitoring & Auditing | CloudWatch, CloudTrail | Metrics, logs, monitoring, and API activity auditing |
| Database Security | RDS, Aurora, DynamoDB | Access control, encryption, backups, and database security concepts |
| Edge & Web Security | CloudFront, Route 53, AWS WAF | Content delivery, DNS, web application filtering concepts |

## Security Controls & Practices

The projects explore and demonstrate security practices including:

- **Least privilege:** Granting workloads only the permissions required for their tasks.
- **Identity-based access control:** Using IAM roles and policies to control access to AWS resources.
- **Temporary credentials:** Using IAM roles rather than embedding long-term access keys in EC2 workloads.
- **Network segmentation:** Separating public and private resources through subnet and routing design.
- **Traffic restrictions:** Limiting inbound access through security group rules.
- **Encryption at rest:** Applying encryption to supported storage resources.
- **Secure transport:** Exploring HTTPS enforcement and secure communication.
- **Monitoring and auditing:** Examining CloudWatch metrics and CloudTrail activity.
- **Permission validation:** Testing allowed and denied actions to verify access boundaries.

## Evidence & Validation

Each project will include relevant evidence to support the configurations and results documented.

| Evidence | Purpose |
|---|---|
| Architecture diagrams | Show resource relationships and network design |
| AWS Console screenshots | Demonstrate resource configurations |
| CLI output | Provide evidence of commands and validation |
| IAM policy documents | Show permissions and access boundaries |
| Connectivity tests | Verify communication between resources |
| Permission tests | Demonstrate allowed and denied actions |
| Troubleshooting records | Explain issues, investigation, and resolution status |
| Technical notes | Explain configuration decisions and security implications |

## Repository Structure

```text
AWS-Cloud-Infrastructure-and-Security-Labs/
│
├── README.md
│
├── 01-account-setup-and-security/
├── 02-vpc-networking-and-security/
├── 03-ec2-and-linux-administration/
├── 04-elastic-block-storage/
├── 05-cloud-monitoring-and-auditing/
├── 06-s3-storage-and-security/
├── 07-elastic-file-system/
├── 08-iam-and-access-management/
├── 09-application-load-balancing/
├── 10-serverless-computing/
├── 11-database-services-and-security/
└── 12-cloudfront-route53-and-waf/
```

## Tools & Technologies

| Category | Tools |
|---|---|
| Cloud Platform | Amazon Web Services (AWS) |
| Operating System | Ubuntu Linux |
| Command Line | AWS CLI, Linux Shell, Windows PowerShell |
| Remote Administration | SSH |
| Web Server | Nginx |

## Documentation Approach

Each project is documented using a consistent technical structure:

1. Project overview and objectives
2. Architecture and resource design
3. AWS services and configurations
4. Implementation and key decisions
5. Security considerations
6. Testing and validation
7. Troubleshooting and findings
8. Lessons learned

## Cost & Security Considerations

These projects are conducted in a personal AWS learning environment. Resource usage and potential charges are considered during implementation.

Sensitive information such as access keys, private SSH keys, passwords, account identifiers, and other credentials will not be published in this repository.


**Author:** [Chidalu Cynthia](https://github.com/Chidalu-Cynthia)

[GitHub Profile](https://github.com/Chidalu-Cynthia)
