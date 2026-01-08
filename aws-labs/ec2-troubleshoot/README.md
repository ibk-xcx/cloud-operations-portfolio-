## Issue Summary 
An EC2 instance became unreachable due to inbound security group rules being removed, blocking SSH access. 
## Diagnosis - Verified instance was running with 3/3 status checks passed (take screenshot) - Reviewed system logs, no boot errors found (take screenshot) - Checked CloudWatch metrics, instance showed activity but no inbound connections (take screenshot) - Inspected security group inbound rules and identified missing SSH access (take screenshot) 
## Resolution - Re-added inbound rules for SSH (22) - Verified connectivity restored via SSH (take screenshot) 
## Preventive Actions - Apply change control to security group modifications - Use baseline security group templates - Enable monitoring alerts for connectivity failures
