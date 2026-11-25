
# AWS EBS Storage Lab

## 1. Project Overview and Objectives

Configured Amazon Elastic Block Store (EBS) to provide persistent block storage for an EC2 instance. The project focused on volume management, attachment, Linux disk operations, and data backup.

## 2. Architecture and Resource Design

Created an EBS volume and attached it to an Ubuntu EC2 instance.

## 3. AWS Services and Configurations

- **Amazon EBS:** Created and configured an EBS volume.

  ![Created EBS Volume](screenshots/Created%20EBS%20Volume.png)

- **EC2:** Attached the EBS volume to an EC2 instance.

  ![EBS Volume Attached to EC2](screenshots/EBS%20Volume%20attached%20to%20EC2.png)

- **Ubuntu Linux:** Formatted and mounted the attached volume.

  ![EBS Volume Formatted and Mounted in Ubuntu](screenshots/Volume%20formatted%20and%20mounted%20in%20Ubuntu..png)

- **Storage Testing:** Created test files on the mounted volume to verify storage functionality.

  ![Test File Created on Mounted EBS Volume](screenshots/Test%20file%20created%20on%20the%20mounted%20volume..png)

- **EBS Snapshots:** Created a snapshot for storage backup.

  ![EBS Snapshot Created](screenshots/Created%20snapshot.png)

## 4. Implementation and Key Decisions

- Created and attached the EBS volume to the EC2 instance.
- Formatted the volume with a Linux filesystem.
- Mounted the volume in Ubuntu.
- Created test files to verify storage functionality.
- Created an EBS snapshot for backup.

## 5. Security Considerations

- Considered the importance of protecting persistent block storage.
- Recognised snapshots as an important part of data backup and recovery.
- Considered access to attached storage through the EC2 instance.

## 6. Testing and Validation

- Verified volume attachment to the EC2 instance.
- Confirmed that the volume was formatted and mounted in Ubuntu.
- Created test files on the mounted volume.
- Created an EBS snapshot.

## 7. Troubleshooting and Findings

Explored how EBS volumes provide persistent block storage independently of the EC2 instance's operating system filesystem operations.

## 8. Lessons Learned

- Managing EBS volumes and attaching them to EC2 instances.
- Formatting and mounting block storage in Ubuntu.
- Understanding persistent storage.
- Creating snapshots for backup and recovery.
