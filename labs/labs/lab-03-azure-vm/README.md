# 📘 Lab 03 - Azure Virtual Machine Deployment

## 📅 Date
04-Apr-2026

---

## 🎯 Objective
Create and configure an Azure Virtual Machine (Windows/Linux) using Azure CLI and Portal

---

## ⚙️ Steps Performed
- Created Resource Group
- Created Virtual Network and Subnet
- Created Virtual Machine
- Configured username and password
- Opened required ports (RDP/SSH)
- Connected to VM

---

## 🔄 Changes from Original Lab
- Used Central India region instead of default
- Used Standard_D2s_v3 size
- Custom VNet created

---

## ❌ Issues Faced
- VM creation failed due to quota limit
- RDP not connecting initially

---

## ✅ Fix / Solution
- Changed VM size to available SKU
- Opened port 3389 in NSG

---

## 💻 Commands Used
```bash
# Create Resource Group
az group create --name prod-vms-rg --location centralindia

# Create VM
az vm create \
  --resource-group prod-vms-rg \
  --name prod-win-vm-01 \
  --image Win2022Datacenter \
  --size Standard_D2s_v3 \
  --admin-username azureadmin \
  --admin-password "Azure@12345"

# Open RDP Port
az vm open-port --port 3389 --resource-group prod-vms-rg --name prod-win-vm-01
