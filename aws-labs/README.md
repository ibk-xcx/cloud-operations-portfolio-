# S3 Access Incident – IAM Permission Failure

## Issue Summary
An EC2 instance was unable to access an S3 bucket due to missing IAM permissions.

---

## Diagnosis

### S3 Access Attempt from EC2
- Attempted S3 access from EC2 using AWS CLI

![S3 Access Attempt](images/iam-before-removal.png)

---

### AccessDenied Error Observed
- Received `AccessDenied` error when attempting to list S3 buckets

![S3 Access Denied Error](images/access-denied.png)

---

### IAM Role Permission Review
- Reviewed IAM role and confirmed S3 permissions were missing

![IAM Role Missing S3 Permissions](images/iam-after-removal.png)

---

## Root Cause
The IAM role attached to the EC2 instance did not include policies allowing S3 access, causing AWS to deny all S3 requests by default.

---

## Resolution

### IAM Permissions Restored
- Reattached appropriate S3 permissions to the IAM role

![IAM Role S3 Permissions Restored](images/reattached-iam.png)

---

### Access Verification
- Verified access restoration via AWS CLI

![S3 Access Restored](images/s3-access-restored.png)

---

## Preventive Actions
- Apply least-privilege IAM policies  
- Implement change control for IAM modifications  
- Periodically audit IAM role permissions
