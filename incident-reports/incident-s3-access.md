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
Bucket policy denied `s3:GetObject` permissions for all principals.

---

## 4. Resolution
- Updated bucket policy to allow `s3:GetObject` for the intended users/principals.  
- Verified access was restored to public assets.  

---

## 5. Preventive Actions
- Apply version-controlled policies for S3 buckets.  
- Implement monitoring/alerts for access denied errors.  
- Review bucket policies before deployment.

