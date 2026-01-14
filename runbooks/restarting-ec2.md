# RUNBOOK – Restarting a Failed EC2 Instance

## Purpose
Guide for restoring service if an EC2 instance becomes unresponsive.

## Steps
1. Log into AWS Console → EC2  
2. Check instance status checks  
3. Review system logs for boot errors  
4. Attempt soft reboot  
5. If unresponsive → stop and start instance  
6. Validate:  
   - App reachable  
   - Ports open  
   - CPU/Memory normal  
7. Update incident ticket  

