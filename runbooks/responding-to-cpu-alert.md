# RUNBOOK – Responding to High CPU CloudWatch Alarm

## Trigger
CPU > 70% for 5+ minutes.

## Steps
1. Check CloudWatch metrics (CPU, network, disk)  
2. SSH into instance & run:  
   - top  
   - ps aux --sort=-%cpu  
3. Identify heavy processes  
4. Restart service or scale instance  
5. Add notes to incident ticket  

