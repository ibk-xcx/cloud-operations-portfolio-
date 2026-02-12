# CHANGE REQUEST FORM

**Change ID:** CR-2026-001  
**Requestor:** Cloud Operations (Lab Simulation)  
**Description:**  
Implement CloudWatch alarm for EC2 instance "the-divide" to trigger notification when CPU utilization exceeds 70%. Additionally, resize instance from t3.micro to t3.small to improve performance stability.

**Risk Level:** Medium  

**Impact:**  
- Brief application interruption during instance resize (restart required)  
- No data loss expected  
- Monitoring alert will improve proactive response to performance issues  

**Backout Plan:**  
- Revert instance type back to t2.micro if performance or cost impact is unacceptable  
- Disable or adjust alarm threshold if false positives occur  
- Restore previous configuration from documented baseline  

**Approver:** Change Manager (Lab Simulation)  

**Scheduled Date:** 2026-01-13  

