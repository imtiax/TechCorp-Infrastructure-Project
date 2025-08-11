# Troubleshooting Guide

## Common Issues and Solutions

### Azure AD Issues
**Problem:** Can't sign in with new user
**Solution:** 
1. Check if user is enabled
2. Verify password hasn't expired
3. Ensure MFA is properly configured

**Problem:** Group membership not working
**Solution:**
1. Check group assignments
2. Allow 15 minutes for propagation
3. Clear browser cache

### Key Vault Issues
**Problem:** Can't access secrets
**Solution:**
1. Check access policies
2. Verify user permissions
3. Ensure Key Vault is not behind firewall

### Monitoring Issues
**Problem:** No data in Log Analytics
**Solution:**
1. Check VM agent status
2. Verify workspace connection
3. Wait 15 minutes for data ingestion

### Backup Issues
**Problem:** Backup job failing
**Solution:**
1. Check VM is running
2. Verify backup policy
3. Check storage account permissions

## Emergency Procedures
1. **VM Down:** Check status, restart if needed
2. **High CPU Alert:** Connect to VM, check processes
3. **Backup Failure:** Check vault status, retry manually
4. **Security Alert:** Review logs, take appropriate action

