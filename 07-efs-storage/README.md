
# AWS EFS Storage Lab

## 1. Project Overview and Objectives

Configured Amazon Elastic File System (EFS) and mounted shared storage on an Ubuntu EC2 instance. The project focused on network file storage, NFS connectivity, and data persistence.

## 2. Architecture and Resource Design

Created an encrypted EFS file system with mount targets across two Availability Zones and connected it to an Ubuntu EC2 instance.

## 3. AWS Services and Configurations

- **Amazon EFS:** Created an encrypted file system.

  ![Encrypted EFS File System Created](screenshots/Created%20an%20encrypted%20EFS%20file%20system.png)

- **Mount Targets:** Configured mount targets across two Availability Zones.
- **Security Groups:** Configured NFS traffic on TCP port `2049`.

  ![EFS NFS Security Group Inbound Rule](screenshots/NFS%20security-group%20inbound%20rule%20(TCP%202049)..png)

- **Ubuntu EC2:** Mounted the EFS file system on the instance.

  ![Successful EFS Mount on Ubuntu](screenshots/Successful%20EFS%20mount%20on%20Ubuntu..png)

- **Data Persistence:** Created a test file and verified its persistence after unmounting and remounting EFS.

  ![EFS Data Persistence Verified](screenshots/Created%20a%20test%20file%20and%20verified%20data%20persistence%20after%20unmounting%20and%20remounting%20EFS.png)

## 4. Implementation and Key Decisions

- Created an encrypted EFS file system.
- Configured mount targets across two Availability Zones.
- Configured NFS access between the EC2 instance and EFS.
- Mounted the file system on Ubuntu.
- Created a test file and verified data persistence after remounting.

## 5. Security Considerations

- Enabled encryption at rest for the EFS file system.
- Used security group rules to control NFS access.
- Restricted NFS access to the EC2 instance security group.

## 6. Testing and Validation

- Verified the EFS mount on Ubuntu.
- Created a test file on the mounted file system.
- Confirmed that the file remained accessible after unmounting and remounting.

## 7. Troubleshooting and Findings

Initially encountered a connection timeout because the EFS security group's inbound NFS rule did not specify the EC2 instance security group as its source. Identified and corrected the missing source configuration.

## 8. Lessons Learned

- Configuring encrypted EFS storage.
- Understanding EFS mount targets and Availability Zones.
- Configuring NFS access through security groups.
- Mounting shared file storage on Linux.
- Verifying data persistence across mount operations.
