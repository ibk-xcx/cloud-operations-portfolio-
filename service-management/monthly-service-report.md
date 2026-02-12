# MONTHLY SERVICE REPORT – SAMPLE

**Service:** EC2-Hosted Web Application  
**Supporting Services:** S3 Static Content  
**Reporting Period:** January 2026  

---

## 1. Availability Summary
- Achieved uptime: 99.7%
- No full-service outages recorded
- One performance degradation incident (P2)

---

## 2. Incident Summary
- P1 (Critical Outage): 0  
- P2 (Major Degradation): 1  
- P3 (Partial Impact): 2  
- P4 (Minor/Informational): 0  

---

## 3. Incident Breakdown & Root Causes
- Security Group misconfiguration blocked SSH access
- IAM permission issue caused S3 AccessDenied error
- High CPU utilization caused temporary application slowdown

---

## 4. Monitoring & Alerts
- CloudWatch CPU alarm configured (>70%)
- Status check monitoring enabled
- SNS email notifications active
- Billing dashboard reviewed for anomaly detection

---

## 5. Improvements Implemented
- Implemented CPU utilization alarm threshold
- Improved security group change controls
- Reviewed IAM role permissions (AmazonS3FullAccess for recovery)
- Evaluating Auto Scaling for performance resilience

---

## 6. Next Month Focus
- Implement Auto Scaling policy
- Apply least-privilege IAM policy refinement
- Conduct load testing validation
- Expand monitoring dashboard metrics

