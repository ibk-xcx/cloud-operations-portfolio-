# SERVICE LEVEL AGREEMENT (SLA)

## 1. Service Scope
- Service: EC2-hosted application
- Supporting Services: S3 static content bucket
- Service Owner: Cloud Operations (Lab Simulation)


## 2. Availability Target
- 99.5% uptime monthly
- Availability measured using:
  - EC2 Status Checks
  - Application reachability
  - CloudWatch monitoring metrics


## 3. Incident Severity & Response Targets

| Severity | Description | Response Time | Resolution Target |

| P1 | Full service outage | 15 minutes | 4 hours |
| P2 | Major degradation (e.g., high CPU slowdown) | 30 minutes | 8 hours |
| P3 | Partial impact (e.g., S3 access denied) | 4 hours | 24 hours |
| P4 | Minor issue / informational | 24 hours | Best effort |


## 4. Monitoring & Alerting
- CloudWatch Metrics:
  - CPUUtilization
  - StatusCheckFailed (System & Instance)
  - NetworkIn / NetworkOut
  - DiskReadOps / DiskWriteOps
- S3 Metrics:
  - BucketSizeBytes
  - NumberOfObjects
  - Request metrics
- CloudWatch Alarms:
  - CPU > 70%
  - Status check failure
- SNS email notifications
- AWS Billing monitoring dashboard


## 5. Reporting & Documentation
- Incident reports (EC2 outage, S3 access issue, performance slowdown)
- CloudWatch dashboard reviews
- Monthly service performance summary


## 6. Objective
To ensure proactive monitoring, rapid incident response, and continuous service reliability through structured operational practices.

