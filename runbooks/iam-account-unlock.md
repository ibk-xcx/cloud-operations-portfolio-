# RUNBOOK – IAM Account Unlock

1. Verify identity  
2. Reset password via IAM → Users → select user → Security credentials tab → Console password → Manage → Reset password  
3. Confirm MFA setup → Users → select user → Security credentials tab → Assigned MFA device → Manage → Deactivate and re-assign if locked out
4. Review policy → Users → select user → Permissions Check inline policies and attached policies → Also check Groups → user’s group policies → Look for Explicit Deny 
5. Document actions in ticket  

