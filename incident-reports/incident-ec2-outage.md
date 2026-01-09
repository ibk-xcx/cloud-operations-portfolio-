# INCIDENT REPORT – EC2 Instance Connectivity Outage

**Incident ID:** INC-2026-001  
**Date:** 2026-01-08  
**Severity:** P2  
**Service Impacted:** EC2-hosted application  
**Reporter:** Ibukun Ajagunna (Lab Simulation)

---

## 1. Summary
An EC2 instance became unreachable due to a misconfigured security group that blocked all inbound traffic, including SSH and HTTP access.

---

## 2. Impact
- Application was unavailable for approximately 15 minutes  
- Users were unable to access the service during this period  

---

## 3. Timeline

| Time | Event |
|------|------|
| 10:00 | Attempted access to EC2 via browser and SSH failed |
| 10:02 | Verified instance state and status checks (passed) |
| 10:05 | Inspected security group and identified missing inbound rules |
| 10:08 | Updated security group to allow SSH (22) and HTTP (80) |
| 10:10 | Connectivity restored and service confirmed operational |

---

## 4. Root Cause
Inbound security group rules were removed, preventing external access to the EC2 instance.

---

## 5. Resolution
- Re-added inbound rules for SSH (port 22) and HTTP (port 80)
- Validated recovery via successful SSH connection and browser access

---

## 6. Preventive Actions
- Apply configuration baselines for security groups  
- Enforce change control for network-related modifications  
- Implement monitoring and alerts for connectivity failures

