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

## Cost Estimate
- **Daily Cost:** Approximately $3-5 USD
- **Monthly Cost:** Approximately $90-150 USD
- **Note:** Stop VMs when not in use to save costs

## Next Steps
1. Install Active Directory on DC01
2. Configure web server on WebServer01
3. Implement backup strategies
4. Add monitoring and alerting
