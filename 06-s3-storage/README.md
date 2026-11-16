# AWS S3 Storage Lab

## Overview
Configured Amazon S3 for object storage and tested bucket versioning and object recovery.

## Configurations & Activities
- Created the `cloudsecurity-storage-lab-2026` bucket.
![S3 Bucket Created](screenshots/Created%20Bucket.png)
- Created and uploaded `storage-lab-notes.txt`.
- Enabled bucket versioning.
![S3 Bucket Versioning Enabled](screenshots/Enabled%20bucket%20versioning.png)
- Modified the file by adding Version 2 content and uploaded it again.
- Verified that S3 retained two versions of the object.
- Downloaded the older version and confirmed that its original content was preserved.
- Verified server-side encryption (SSE-S3) and S3 Standard storage class.

## Key Skills
S3 bucket management · Object uploads · Versioning · Object recovery · Data protection
