# EC2 Connectivity Issue – Security Group Misconfiguration

## Issue Summary
An EC2 instance became unreachable due to inbound security group rules being removed, blocking SSH access.

## Diagnosis

### EC2 Instance Status Check
- Verified instance was running with 3/3 status checks passed  
 

![EC2 Status Check Passed](images/checks-passed.png)

---

### System Logs Review
- Reviewed system logs and confirmed no boot errors  
 

![EC2 System Logs](images/system-log.png)

---

### CloudWatch Metrics
- Checked CloudWatch metrics; instance showed activity but no inbound connections  


![CloudWatch Metrics](images/metrics-view.png)

---

### Security Group Inspection
- Inspected security group inbound rules and identified missing SSH access  


![Security Group Missing SSH Rule](images/ssh-timeout.png)

---

## Resolution
- Re-added inbound rule to allow SSH (port 22) from my IP

![Security Group SSH Restored](images/sg-after-fix.png)

- Verified connectivity restored via SSH

![Successful SSH Connection](images/successful-ssh-session.png)

---

## Preventive Actions
- Apply change control to security group modifications
- Use baseline security group templates
- Enable monitoring alerts for connectivity failures
