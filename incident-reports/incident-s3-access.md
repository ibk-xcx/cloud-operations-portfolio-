# INCIDENT REPORT – S3 Access Denied

**Incident ID:** INC-2025-002  
**Severity:** P3  
**Service:** S3 static content bucket  
**Date:** 2026-01-09

---

## 1. Summary
Users were unable to access files stored in an S3 bucket due to incorrect bucket policy.

---

## 2. Impact
- Public assets not loading  
- Application partially broken

---

## 3. Root Cause
The IAM role accessing the S3 bucket did not have the required permissions at the time of the incident. Required S3 permissions were missing, resulting in `AccessDenied` errors when attempting to retrieve objects.


---

## 4. Resolution
- Attached the `AmazonS3FullAccess` policy to the affected IAM role
- Verified restored access to S3 objects via AWS CLI and console  

---

## 5. Preventive Actions
- Apply version-controlled policies for S3 buckets.  
- Implement monitoring/alerts for access denied errors.  
- Review bucket policies before deployment.

