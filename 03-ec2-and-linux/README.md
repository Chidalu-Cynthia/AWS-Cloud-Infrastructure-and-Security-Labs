
# AWS EC2 & Linux Administration Lab

## 1. Project Overview and Objectives

Deployed and configured an Ubuntu EC2 instance within my custom VPC. The project focused on compute deployment, secure remote access, instance security, and basic Linux administration.

## 2. Architecture and Resource Design

Deployed an Ubuntu EC2 instance in a public subnet within the custom VPC, with a public IPv4 address for remote SSH access.

## 3. AWS Services and Configurations

- **Amazon EC2:** Launched an Ubuntu Server 26.04 LTS instance using the `t3.micro` instance type.

  ![Launched Ubuntu EC2 Instance](screenshots/Launched%20Ubuntu%20EC2%20Instance.png)

- **Instance Configuration:** Configured the instance with an 8 GiB encrypted EBS root volume, IMDSv2 enforcement, and Standard CPU credit mode.

  ![EC2 Instance Configuration](screenshots/Instance%20Configuration.jpeg)

- **Security Group:** Restricted SSH access (TCP port 22) to my IP address.
- **SSH Authentication:** Used key-based authentication to connect securely to the instance.

## 4. Implementation and Key Decisions

- Deployed the instance in the public subnet with a public IP address.
- Used SSH key authentication instead of password-based remote access.
- Connected successfully to the Ubuntu instance.

  ![Successful SSH Connection](screenshots/Successful%20SSH%20Connection.png)

- Updated and maintained the Ubuntu operating system.

  ![Ubuntu System Updates](screenshots/Updated%20and%20maintained%20the%20Ubuntu%20system..png)

- Practised Linux commands, file management, permissions, users, and groups.

  ![File and Directory Permissions Practice](screenshots/Explored%20file%20and%20directory%20permissions.png)

## 5. Security Considerations

- Encrypted the EBS root volume.
- Restricted inbound SSH access to my IP address.
- Enforced IMDSv2 for instance metadata access.
- Used SSH key-based authentication.
- Set CPU credit mode to Standard to avoid surplus CPU credit charges.

## 6. Testing and Validation

- Confirmed successful SSH access to the EC2 instance.
- Verified instance and system status checks passed.
- Updated Ubuntu packages and practised Linux file permissions.

## 7. Troubleshooting and Findings

Initially encountered an SSH connection timeout caused by using an incorrect public IP address. Correcting the IP address resolved the connection issue.

## 8. Lessons Learned

- Deploying and configuring EC2 instances within a custom VPC.
- Securing remote access using SSH keys and security group rules.
- Understanding EBS encryption and IMDSv2.
- Performing basic Ubuntu administration.
- Managing Linux files, permissions, users, and groups.
