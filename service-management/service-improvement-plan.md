# SERVICE IMPROVEMENT PLAN (SIP)

## 1. Issue
Recurring S3 access issues resulting in `AccessDenied` errors impacting application functionality.

---

## 2. Root Cause
Inconsistent IAM role and bucket permission management, leading to misaligned access controls and insufficient validation after changes.

---

## 3. Action Plan
- Implement least-privilege IAM policies instead of temporary full-access permissions  
- Standardize S3 permission change process with documented approval workflow  
- Enable and review IAM Access Analyzer weekly  
- Validate access changes using AWS CLI before closing change requests  
- Include S3 permission checks in monthly service review  

---

## 4. Expected Outcome
- Reduction in permission-related incidents  
- Improved visibility into access control risks  
- Stronger governance and compliance posture  
- Faster resolution of future S3 access issues  

