
# AWS S3 Storage Lab

## 1. Project Overview and Objectives

Configured Amazon S3 for object storage, versioning, data protection, and object recovery.

## 2. Architecture and Resource Design

Created the S3 bucket `cloudsecurity-storage-lab-2026` to store and manage objects.

## 3. AWS Services and Configurations

- **Amazon S3:** Created the `cloudsecurity-storage-lab-2026` bucket.

  ![S3 Bucket Created](screenshots/Created%20Bucket.png)

- **Object Upload:** Created and uploaded `storage-lab-notes.txt` to the bucket.

  ![Text File Uploaded to S3 Bucket](screenshots/Uploaded%20text%20file%20to%20Bucket.png)

- **Bucket Versioning:** Enabled versioning to preserve multiple versions of objects.

  ![S3 Bucket Versioning Enabled](screenshots/Enabled%20bucket%20versioning.png)

- **Data Protection:** Kept Block Public Access enabled, disabled ACLs, and verified default SSE-S3 encryption.
- **Bucket Policy:** Configured a policy to deny requests made over insecure transport.

## 4. Implementation and Key Decisions

- Uploaded the initial version of `storage-lab-notes.txt`.
- Modified the file and uploaded it again to create a second version.
- Downloaded the older version and verified that its original content was preserved.
- Used versioning to support object recovery.

## 5. Security Considerations

- Kept S3 Block Public Access enabled.
- Disabled ACLs to manage access through policies.
- Used server-side encryption with Amazon S3-managed keys (SSE-S3).
- Enforced secure transport through a bucket policy.

## 6. Testing and Validation

- Verified that the bucket was created.
- Confirmed that two versions of the object were retained.
- Downloaded and checked the older object version.
- Verified SSE-S3 encryption and the S3 Standard storage class.
- Tested that anonymous access was denied.

## 7. Troubleshooting and Findings

Object versioning preserved the previous file version after a modified copy was uploaded. This allowed the older content to be retrieved without losing the original version.

## 8. Lessons Learned

- Managing S3 buckets and objects.
- Using versioning to preserve object history.
- Retrieving previous object versions.
- Applying S3 access controls and encryption.
- Enforcing secure transport for bucket requests.
