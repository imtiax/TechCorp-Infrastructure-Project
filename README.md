# TechCorp Infrastructure Project

## Overview
This project demonstrates the setup of a basic company infrastructure in Microsoft Azure.

## Architecture
- **Resource Groups:** 3 (Production, Development, Network)
- **Virtual Network:** 10.0.0.0/16
- **Subnets:** 3 (Web, App, Database)
- **Virtual Machines:** 2 (Windows DC, Linux Web Server)
- **Security Groups:** 3 (Web, App, Database NSGs)

## Resources Created
### Resource Groups
- TechCorp-Prod-RG (East US)
- TechCorp-Dev-RG (East US)
- TechCorp-Network-RG (East US)

### Network Components
- TechCorp-VNet (10.0.0.0/16)
  - Web-Subnet (10.0.1.0/24)
  - App-Subnet (10.0.2.0/24)
  - Database-Subnet (10.0.3.0/24)

### Virtual Machines
- DC01 (Windows Server 2019) - Web-Subnet
- WebServer01 (Ubuntu 20.04) - App-Subnet

### Security Groups
- Web-NSG (HTTP, HTTPS, RDP allowed)
- App-NSG (SSH allowed)
- Database-NSG (Basic rules)

## Connection Information
- **Windows VM:** RDP to DC01 public IP
- **Linux VM:** SSH to WebServer01 public IP
- **Credentials:** azureuser / TechCorp123!@# (Windows)

## Security & Monitoring Implementation

## Overview
Enhanced the basic infrastructure with enterprise-level security and monitoring capabilities.

## Components Added

### Azure Active Directory
- **Security Groups Created:**
  - IT-Department
  - HR-Department
  - Azure-Administrators

- **Users Created:**
  - john.smith (IT Administrator)
  - jane.doe (HR Manager)

- **Security Features:**
  - Multi-factor authentication for administrators
  - Conditional access policies
  - Role-based access control

### Azure Key Vault
- **Vault Name:** techcorp-keyvault-001
- **Stored Secrets:**
  - DC01-AdminPassword
  - WebServer01-SSHKey
- **Access Policies:** Configured for admin users

### Monitoring & Logging
- **Log Analytics Workspace:** TechCorp-LogAnalytics
- **Connected Resources:** Both VMs sending logs
- **Performance Monitoring:** CPU, Memory, Disk metrics
- **Custom Dashboards:** TechCorp-Operations-Dashboard

### Backup Configuration
- **Recovery Services Vault:** TechCorp-Backup-Vault
- **Backup Policy:** Daily-Backup-Policy
- **Protected Resources:** DC01, WebServer01
- **Retention:** 30 days

### Security Alerts
- **Alert Rules:**
  - High-CPU-DC01 (>80% CPU usage)
  - Low-Memory-DC01 (<500MB available)
- **Action Groups:** IT-Alerts (email notifications)
- **Notification Email:** [your-email@domain.com]

## Architecture Diagram
Azure AD
├── Users (john.smith, jane.doe)
├── Groups (IT-Department, HR-Department, Azure-Administrators)
└── Conditional Access Policies
Key Vault
├── DC01-AdminPassword
└── WebServer01-SSHKey
Monitoring
├── Log Analytics Workspace
├── Performance Dashboards
└── Alert Rules
Backup
├── Recovery Services Vault
└── Daily Backup Policies

## Security Best Practices Implemented
1. Multi-factor authentication for privileged accounts
2. Centralized secret management with Key Vault
3. Comprehensive monitoring and alerting
4. Regular automated backups
5. Role-based access control
6. Conditional access policies

## Next Steps
1. Implement Azure Security Center recommendations
2. Add more granular monitoring rules
3. Configure automated remediation
4. Set up disaster recovery testing
5. Implement compliance reporting

## Cost Optimization
- Use free tiers where possible
- Set up budget alerts
- Review and optimize resources monthly
- Consider reserved instances for long-term use

## Time Investment
- **Duration:** 4 days
- **Daily Time:** 2-3 hours

## Skills Developed
- Azure Active Directory administration
- Key Vault management
- Azure Monitor configuration
- Backup and recovery planning
- Security alert configuration
- Dashboard creation and management

