# INCIDENT REPORT – Application Slowdown

**Incident ID:** INC-2026-003  
**Date:** 2026-01-13  
**Severity:** P2  
**Service Impacted:** EC2-based application  
**Reporter:** Self (Lab Simulation)

---

## 1. Summary
Application experienced slow response times due to high CPU usage triggered by a load spike.

---

## 2. Impact
- Response times increased from ~120ms to ~3 seconds  
- Some customer sessions experienced timeouts  

---

## 3. Findings
CloudWatch metrics indicated CPU utilization sustained above 85% for approximately 10 minutes, triggering a performance degradation.

---

## 4. Resolution`
- Terminated high-CPU/stuck processes
- Restarted application service to restore normal performance

---

## 5. Preventive Actions
- Implement Auto Scaling based on CPU thresholds  
- Maintain CloudWatch alarm for CPU utilization > 70%  
- Perform load and performance testing during change deployments

