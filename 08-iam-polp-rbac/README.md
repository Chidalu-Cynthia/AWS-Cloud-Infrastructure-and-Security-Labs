
# AWS IAM: Principle of Least Privilege & Role-Based Access Control

## 1. Project Overview and Objectives

This project focused on using AWS Identity and Access Management (IAM) to control access between an EC2 instance and an Amazon S3 bucket.

The objective was to apply the principle of least privilege by granting an EC2 instance only the S3 permissions required to list and download objects, while preventing upload and deletion operations.

## 2. Architecture and Resource Design

The lab used an IAM role to provide temporary AWS permissions to an Ubuntu EC2 instance.

**Access flow:**

`Ubuntu EC2 Instance → IAM Role → IAM Policy → Amazon S3 Bucket`

The role trusted the EC2 service, while its attached permissions policy controlled access to the S3 bucket.

## 3. AWS Services and Configurations

- **AWS IAM Policy:** Created the customer-managed policy `CloudSecurity-S3-ReadOnly-Lab-Policy`, allowing `s3:ListBucket` on the specified bucket and `s3:GetObject` on its objects.

  ![Created IAM policy](screenshots/Created%20IAM%20policy.png)

- **AWS IAM Role:** Created `CloudSecurity-EC2-S3-ReadOnly-Role` with EC2 as its trusted service.

  ![Created IAM Role](screenshots/Created%20IAM%20Role.png)

- **IAM Role Permissions:** Attached the customer-managed S3 read-only policy to the IAM role.

  ![Attached IAM Policy to Role](screenshots/Attached%20IAM%20Policy%20to%20Role.png)

- **Amazon EC2:** Attached the IAM role to the `CloudSecurity-EC2` Ubuntu instance.

  ![Attached IAM Role to EC2](screenshots/Attached%20IAM%20Role%20to%20EC2.png)

- **AWS CLI:** Installed AWS CLI on the EC2 instance to verify its identity and test S3 permissions.

## 4. Implementation and Key Decisions

The customer-managed policy granted only these permissions:

- `s3:ListBucket` — allowed listing the contents of `cloudsecurity-storage-lab-2026`.
- `s3:GetObject` — allowed downloading objects from the bucket.

The policy did not grant `s3:PutObject` or `s3:DeleteObject`.

The IAM role used an EC2 trust policy that allowed the EC2 service to assume the role through `sts:AssumeRole`.

After attaching the role to the EC2 instance, I installed AWS CLI on Ubuntu and used the instance's assigned role instead of configuring long-term access keys.

## 5. Security Considerations

- Applied the principle of least privilege by granting only the required S3 read permissions.
- Used an EC2 IAM role instead of storing long-term AWS access keys on the instance.
- Separated the role's trust policy from its permissions policy.
- Restricted access to the specified S3 bucket and its objects.
- Verified that upload and deletion operations were not permitted.

## 6. Testing and Validation

I used AWS CLI commands on the EC2 instance to verify the role and test its permissions.

**Identity verification:**

`aws sts get-caller-identity`

The returned assumed-role identity confirmed that the EC2 instance was using the assigned IAM role.

![Verified IAM Role with STS](screenshots/Verified%20IAM%20Role%20with%20STS.png)

**Allowed operations:**

Listed the bucket contents:

`aws s3 ls s3://cloudsecurity-storage-lab-2026`

Downloaded an existing object:

`aws s3 cp s3://cloudsecurity-storage-lab-2026/storage-lab-notes.txt ./storage-lab-notes.txt`

Both operations succeeded.

**Denied upload operation:**

Attempted to upload an object:

`aws s3 cp iam-upload-test.txt s3://cloudsecurity-storage-lab-2026/iam-upload-test.txt`

The operation returned `AccessDenied`.

**Denied delete operation:**

Attempted to delete an existing object:

`aws s3 rm s3://cloudsecurity-storage-lab-2026/storage-lab-notes.txt`

The operation returned `AccessDenied`.

![Tested IAM Permissions with AWS CLI](screenshots/Tested%20IAM%20Permissions%20with%20AWS%20CLI.png)

![Tested IAM Delete permission](screenshots/Tested%20IAM%20Delete%20permission.png)

I also verified that the original S3 object remained in the bucket.

## 7. Troubleshooting and Findings

The denied upload and delete operations were expected results, not configuration failures.

The role had no applicable `Allow` permissions for `s3:PutObject` or `s3:DeleteObject`. These requests were therefore denied by IAM's default implicit-deny behaviour.

I also confirmed the distinction between the two IAM policies used in the setup:

- **Trust policy:** Determines which service or principal can assume the role.
- **Permissions policy:** Determines which AWS actions the assumed role can perform.

## 8. Lessons Learned

This lab demonstrated how IAM roles provide temporary credentials to EC2 instances without requiring long-term access keys.

I also gained practical experience creating a customer-managed policy, defining a role's trust relationship, attaching the role to an EC2 instance, and validating permissions through AWS CLI.

Most importantly, I learned that effective access control involves verifying both the actions a role is allowed to perform and those it must be prevented from performing.
