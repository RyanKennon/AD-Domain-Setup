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
- Active Directory Domain Services (AD DS)
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

## 1) Create Azure Virtual Machines

### Domain Controller (DC)
- Image: Windows Server 2022 Datacenter
- Size: Minimum 2 vcpus

### Client Machine
- Image: Windows 10 Pro
- Make sure that the DC and Client are on the same subnet

---

## 2) Make the DC's IP address Static

1. Select **domain controller**
2. Select **Network Settings**
3. Open **Network Interface**
4. Select ipconfig1
5. For Private IP address setting choose **Static**
6. Save

---

## 3) Assign the Client the same private IP address as the DC

1. Select **Client virtual machine**
2. Select **Network Settings**
3. Open **Network Interface**
4. Select **DNS Servers**
5. Choose **Custom**
6. Enter the **DC's Private IP address**
7. Save

---

## 4) Install Active Directory Domain Services

1. Log into the **Domain Controller**
2. Open **Server Manager**
3. Select **Add roles and features**
4. On the **Server Roles** tab check **Active Directory Domain Services**
5. Complete the installation

---

## 5) Promote Server to Domain Controller

1. In **Server Manager**, click the notification flag
2. Select **Promote this server to a domain controller**
3. Choose **Add a new forest**
4. Set the root domain name
5. Set the Directory Services Restore Mode (DSRM) password
6. Complete the wizard and reboot the server

---

## 6) Join the Client to the Domain

1. Log into the Client as your orignal local admin
2. 
