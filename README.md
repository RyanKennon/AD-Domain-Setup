<p align="center">
  <img src="https://github.com/user-attachments/assets/7b65e021-0e08-42ae-8da2-f57cd11aceb7" width="300" height="168" alt="image" />
</p>

# Configuring On-Premises Active Directory within Azure VMs

This project documents the deployment of a traditional **on-premises Active Directory environment** hosted within **Microsoft Azure Virtual Machines**.
The goal is to demonstrate foundational identity, authentication, and domain management concepts using cloud-based infrastructure while preserving classic on-prem AD architecture.

---

## Environments and Technologies Used

- Microsoft Azure
- Azure Virtual Network
- Remote Desktop Protocol (RDP)
- PowerShell

---

## Lab Objective

- Deploy A Windows Server domain controller in Azure
- Install and configure Active Directory Domain Services
- Create and configure an Active Directory forest
- Join a Windows client to the domain
- Validate authentication and directory functionality

---

## Step-by-Step Summary

## 1. Create Azure Virtual Machines

Create two Azure virtual machines

### Domain Controller (DC)
